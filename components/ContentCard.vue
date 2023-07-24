<template>
  <div class="ContentCard">
    <div class="card__logo">
      <div class="logo">
        <img src="/ipc.png" alt="" />
      </div>
      <button class="button">
        <span>Go to live app</span>
        <span class="material-symbols-sharp"> arrow_outward </span>
      </button>
    </div>
    <div class="card__content">
      <div class="card__title card">IPC Africa</div>
      <div class="snippet card">
        I built a commerce infrastructure product for Brass that enables users
        to to build and manage multiple stores both physical and online through
        one sophisticated app.
      </div>
    </div>
    <img src="" alt="" class="card__image">
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.ContentCard {
  background-color: rgba(32, 33, 35);
  place-content: center flex-start;
  align-items: center;
  /* background-color: rgb(33, 35, 37); */
  border-radius: 24px;
  display: flex;
  flex: 0 0 auto;
  flex-flow: column nowrap;
  gap: 24px;
  /* height: 630px; */
  overflow: hidden;
  padding: 32px;
  position: relative;
  /* width: 592px; */
  /* will-change: transform; */
  height: 200vh;
}
.card__logo {
  display: flex;
  flex-direction: row;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.logo img {
  height: 35px;
  /* width: 79px; */
}
.button {
  background-color: #00dc82;
  border: 1px solid #24ffa4;
  border-radius: 8px;
  align-items: center;
  display: flex;
  flex-direction: row;
  gap: 8px;
  height: 39px;
  justify-content: center;
  padding: 0;
  max-width: 179px;
  width: 100%;
  font-size: 12px;
  box-shadow: rgba(0, 0, 0, 0.26) 0px 0.637473px 1.14745px -1.125px,
    rgba(0, 0, 0, 0.24) 0px 1.93094px 3.4757px -2.25px,
    rgba(0, 0, 0, 0.192) 0px 5.10423px 9.18761px -3.375px,
    rgba(0, 0, 0, 0.03) 0px 16px 28.8px -4.5px;
    transition: .3s ease-in-out;
}
.button .material-symbols-sharp {
  font-weight: 700;
}
.button:hover {
    opacity: .9;
    gap: 20px;
}
.card {
    color: #d9d9d9;
}
</style>