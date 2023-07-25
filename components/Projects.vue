<template>
  <div class="wrapper">
    <ContentCard
      imageUrl="/ipcwebsite.png"
      cardTitle="IPC Africa"
      span="website"
      snippet="I built a commerce infrastructure product for Brass that enables users
        to to build and manage multiple stores both physical and online through
        one sophisticated app."
        routePath="https://ipc-africa.com/"
    />
    <ContentCard
      imageUrl="/ipcadmin.png"
      cardTitle="IPC Africa"
      span="Admin Web-App"
      snippet="I built a commerce infrastructure product for Brass that enables users
        to to build and manage multiple stores both physical and online through
        one sophisticated app."
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