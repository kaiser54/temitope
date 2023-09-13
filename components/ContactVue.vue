<template>
  <div class="ContentCard">
    <div class="card__logo">contact</div>
    <div class="card__content">
      <div class="card__title card">Get in touch.</div>
      <div class="snippet card">I am happy to serve and be of service</div>
    </div>
    <a
      href="mailto:agboolatemitope070@gmail.com?subject=Regarding%20Contact%20Message"
      target="_blank"
    >
      <button class="button">
        <span>Send me an email</span>
        <span class="material-symbols-sharp"> arrow_outward </span>
      </button>
    </a>
  </div>
</template>
  
  <script>
export default {
  props: {
    routePath: {
      type: String,
      required: true,
    },
    cardTitle: {
      type: String,
      required: true,
    },
    span: {
      type: String,
    },
    snippet: {
      type: String,
    },
    imageUrl: {
      type: String,
      required: true,
    },
  },
};
</script>
  
  <style scoped>
.ContentCard {
  background-color: rgba(32, 33, 35);
  place-content: center flex-start;
  /* align-items: center; */
  /* background-color: rgb(33, 35, 37); */
  border-radius: 24px;
  display: flex;
  flex: 0 0 auto;
  flex-flow: column nowrap;
  gap: 24px;
  /* height: 630px; */
  overflow: hidden;
  padding: 32px;
  /* padding-bottom: 0; */
  position: relative;
  max-width: 592px;
  width: 100%;
  /* will-change: transform; */
  /* height: 200vh; */
}
.card__logo {
  padding: 4px 12px;
  border-radius: 100px;
  display: flex;
  flex-direction: row;
  width: fit-content;
  justify-content: space-between;
  align-items: center;
  background: #151717;
  color: rgba(217, 217, 217, 0.469);
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
  transition: 0.3s ease-in-out;
}
a {
  max-width: 179px;
  width: 100%;
}
.button .material-symbols-sharp {
  font-weight: 700;
}
.button:hover {
  opacity: 0.9;
  gap: 20px;
}
.card__title {
  font-size: 1.4rem;
}
.card {
  color: #d9d9d9;
}
.img {
  width: 300px; /* Set the desired width of the container */
  height: 200px; /* Set the desired height of the container */
  aspect-ratio: 1.155701754385965 / 1;
  flex: none;
  height: var(--framer-aspect-ratio-supported, 456px);
  overflow: visible;
  position: relative;
  width: 527px;
  overflow: hidden; /* Ensure the clipped part of the image is hidden */
  border-radius: 16px 16px 0 0;
}
.img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: top;
}
</style>