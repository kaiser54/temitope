<template>
  <MainLayout>
    <div class="wrapper">
      <div class="image__slider">
        <ImageSlider :images="imageUrls" />
        <ImageSlider :images="imageUrls" />
      </div>
      <div class="image__slider">
        <ImageSlider :images="imageUrls" />
        <ImageSlider :images="imageUrls" />
      </div>
      <Projects />
    </div>
  </MainLayout>
</template>

<script>
import MainLayout from "/layouts/MainLayout.vue";
export default {
  components: { MainLayout },
  data() {
    return {
      imageUrls: [
        "/ipcwebsite.png",
        "/ipcwebsite.png",
        "/ipcwebsite.png",
        // Add more image URLs here
      ],
    };
  },
};
</script>

<style>
.image__slider {
  display: flex;
  gap: 10px;
  margin-bottom: 10px;
}
</style>