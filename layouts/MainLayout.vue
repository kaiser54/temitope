<template>
  <div>
    <div class="wrapper">
      <div class="child">
        <div class="mainlayout">
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
.snippet {
  font-size: 0.86rem;
  line-height: 1.65;
  font-weight: 300;
  color: rgb(209, 213, 219);
}
.page__wrapper {
  padding-top: 88px;
  width: 100%;
  height: 100vh;
  /* background-color: rgba(32, 33, 35); */
}
</style>