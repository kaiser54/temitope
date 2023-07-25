<template>
  <div>
    <div class="wrapper">
      <div class="child" style="position: relative">
        <div class="mainlayout" style="position: fixed">
          <div class="branding">
            <Logo />
            <NavBar />
          </div>
          <div class="hello">
            <div class="title__font">
              Hi👋🏾 , I'm Temitope Agboola,<br />
              a frontend developer.
            </div>
            <div class="hello__msg">
              <p class="snippet">
                I specialize in crafting captivating websites and web
                applications with a focus on user experience. From front-end
                development to responsive design, I take pride in delivering
                high-quality results that engage and delight users.
              </p>
              <p class="snippet">
                With a passion for storytelling through code, I've worked on
                diverse projects, leaving a lasting impact on their users.
                Whether it's e-commerce platforms, informative blogs, or
                innovative web apps, I'm committed to excellence.
              </p>
              <p class="snippet">
                Collaboration is key to my process. I enjoy working with design
                teams, product managers, and clients to bring concepts to
                reality. Let's turn your ideas into a compelling online
                presence!
              </p>
              <p class="snippet">
                Thank you for visiting my portfolio, and I'm excited to work
                with you on your next web adventure!
              </p>
            </div>
          </div>
        </div>
      </div>
      <div class="child">
        <div class="page__wrapper">
          <slot />
          <div class="copyright">
            <!-- <div class="love">BETA version made with ❤️</div> -->
            Copyright © 2000 — 2023, Temitope Agboola. To get a quote, <br />
            please click here. Built using Nuxt with ❤️.
            <div class="love">BETA version</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: row;
  width: 85%;
  margin-inline: auto;
  gap: 32px;
}
.branding {
  display: flex;
  gap: 16px;
  flex-direction: column;
  margin-block: 32px;
}
.logo__icon {
  width: 15%;
}
.logo__icon .cls-1 {
  fill: #00dc82;
}
.cls-1 {
  fill: #ffeacf;
}
.cls-2 {
  fill: #00dc82;
}
.cls-3 {
  fill: #333;
}
.child {
  flex: 1;
}
.hello {
  max-width: 488px;
  display: flex;
  flex-direction: column;
  gap: 32px;
}
.hello__msg {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.page__wrapper {
  padding-block: 88px;
  width: 100%;
  /* height: 100vh; */
  /* overflow: auto; */
  display: flex;
  flex-direction: column;
  gap: 128px;
  /* background-color: rgba(32, 33, 35); */
}
.page__wrapper::-webkit-scrollbar {
  display: none;
}
.copyright {
  font-size: 12px;
  color: #d9d9d9;
  font-weight: 200;
}
.love {
  /* position: absolute; */
  /* bottom: 10px; */
  /* left: 10px; */
  background-color: rgb(255, 255, 255);
  background-color: #00dc82;
  background-color: rgba(32, 33, 35);
  cursor: pointer;
  border-radius: 10px;
  box-shadow: rgba(0, 0, 0, 0.26) 0px 0.637473px 1.14745px -1.125px,
    rgba(0, 0, 0, 0.24) 0px 1.93094px 3.4757px -2.25px,
    rgba(0, 0, 0, 0.192) 0px 5.10423px 9.18761px -3.375px,
    rgba(0, 0, 0, 0.03) 0px 16px 28.8px -4.5px;
  opacity: 1;
  height: 36px;
  overflow: hidden;
  padding-inline: 10px;
  width: fit-content;
  display: flex;
  align-items: center;
  font-size: 12px;
  color: #ffeacf;
  margin-top: 12px;
}

/* Styles for screens with a minimum width of 768px */
@media screen and (max-width: 1290px) {
.wrapper {
  width: 90%;
}
}
</style>