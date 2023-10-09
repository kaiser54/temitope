<template>
  <MainLayout>
    <div class="wrapper">
      <div class="image__slider">
        <ImageSlider :images="imageUrls" />
        <Card>
          <button class="button">
          <span>Akure, NG</span>
        </button>
        </Card>
      </div>
      <!-- <IMGSlider :images="imageUrls"/> -->
      <Projects />
      <ContactVue />
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
        "/ipc.png",
        "/ipcwebsite.png",
        "/ipcadmin.png",
        // Add more image URLs here
      ],
    };
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}
.image__slider {
  display: flex;
  gap: 20px;
  margin-bottom: 10px;
  width: 100%;
}
.button {
  background-color: #3c3c3c;
  border: 1px solid #24ffa4;
  color: white;
  border-radius: 8px;
  align-items: center;
  display: flex;
  flex-direction: row;
  gap: 8px;
  /* height: 39px; */
  justify-content: center;
  padding: 0;
  max-width: 179px;
  width: 100%;
  font-size: 12px;
  box-shadow: rgba(0, 0, 0, 0.26) 0px 0.637473px 1.14745px -1.125px,
    rgba(0, 0, 0, 0.24) 0px 1.93094px 3.4757px -2.25px,
    rgba(0, 0, 0, 0.192) 0px 5.10423px 9.18761px -3.375px,
    rgba(0, 0, 0, 0.03) 0px 16px 28.8px -4.5px;
  transition: 0.3s ease-in-out;
}
</style>