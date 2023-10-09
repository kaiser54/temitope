<template>
  <div class="image-slider">
    <div class="slider-container">
      <div
        class="slider"
        :style="{ transform: `translateY(${slideOffset}px)` }"
      >
        <div v-for="(image, index) in images" :key="index" class="slide">
          <img :src="image" alt="Slide" />
        </div>
      </div>
    </div>
  </div>
</template>
  
  <script>
export default {
  props: {
    images: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      slideOffset: 0,
      currentIndex: 0,
      isDragging: false,
      startDragY: 0,
    };
  },
  computed: {
    totalSlides() {
      return this.images.length;
    },
  },
  methods: {
    handleTouchStart(event) {
      this.isDragging = true;
      this.startDragY = event.touches[0].clientY;
    },
    handleTouchMove(event) {
      if (!this.isDragging) return;

      const deltaY = event.touches[0].clientY - this.startDragY;
      this.slideOffset += deltaY;
      this.startDragY = event.touches[0].clientY;
    },
    handleTouchEnd() {
      this.isDragging = false;

      if (this.slideOffset > 0) {
        this.slideOffset = 0;
      } else if (this.slideOffset < -100 * (this.totalSlides - 1)) {
        this.slideOffset = -100 * (this.totalSlides - 1);
      } else {
        this.currentIndex = Math.round(-this.slideOffset / 100);
        this.slideOffset = -this.currentIndex * 100;
      }
    },
    startAutoSlide() {
      setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % this.totalSlides;
        this.slideOffset = -this.currentIndex * 100;
      }, 5000);
    },
  },
  created() {
    this.startAutoSlide();
  },
};
</script>
  
  <style scoped>
.image-slider {
  width: 200px; /* Adjust the width as needed */
  height: 400px; /* Adjust the height as needed */
  overflow: hidden;
  border-radius: 20px;
  position: relative;
}

.slider-container {
  height: 100%;
  overflow: hidden;
}

.slider {
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease-in-out;
}

.slide {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

img {
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
}
</style>
  