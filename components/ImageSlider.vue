<template>
  <div class="square-card">
    <carousel
      class="carousel"
      :per-page="1"
      :autoplay="true"
      :loop="true"
      :pagination-enabled="true"
    >
      <slide v-for="(image, index) in images" :key="index">
        <img :src="image" alt="Image" />
      </slide>
    </carousel>
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
};
</script>
  
<style scoped>
.square-card {
  width: 286px;
  height: 258px;
  border-radius: 24px;
  overflow: auto;
}
.square-card::-webkit-scrollbar {
  display: none;
}

.carousel {
  display: flex;
  flex-direction: column;
  animation: scrollAnimation 10s linear infinite;
}
@keyframes scrollAnimation {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-50%);
  }
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>

  