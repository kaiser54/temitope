<template>
  <div class="wrapper">
    <ContentCard
      imageUrl="/ipcwebsite.png"
      cardTitle="IPC Africa"
      span="website"
      snippet="a cutting-edge online shopping platform built to deliver an exceptional user experience. Leveraging the power of Nuxt.js and a stack of other advanced technologies, I've created a seamless and feature-rich e-commerce solution that's ready to take your business to the next level."
      routePath="https://ipc-africa.com/"
    />
    <ContentCard
      imageUrl="/ipcadmin.png"
      cardTitle="IPC Africa"
      span="Admin Web-App"
      snippet="a cutting-edge online shopping platform built to deliver an exceptional user experience. Leveraging the power of Nuxt.js and a stack of other advanced technologies, I've created a seamless and feature-rich e-commerce solution that's ready to take your business to the next level."
      routePath="https://admin-ipc-nuxt3.vercel.app/"
    />
  </div>
</template>
   
   <script>
export default {};
</script>
   
<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}
</style>