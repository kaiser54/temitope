<template>
  <div :class="{ animateContainer: isActive }" v-if="isActive">
    <div class="cursor"></div>
    <div class="inner-cursor"></div>
  </div>

  <div class="norm" :class="{ fade: !isActive }">
    <div class="wrapper">
      <Navbar2 />
    </div>
    <slot />
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.isActive = false;
    }, 3500);
  },
  watch: {
    $route() {
      this.isActive = true;
      setTimeout(() => {
        this.isActive = false;
      }, 3500);
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Montserrat:400,400i,700");

.animateContainer {
  position: fixed;
  z-index: 9999999;
  top: 0;
  width: 100%;
  height: 100vh;
  &::before {
    content: "";
    background: #fff;
    width: 100%;
    height: 0%;
    position: absolute;
    bottom: 0;
    transform-origin: bottom;
    transition: 3s cubic-bezier(0.22, 0.73, 0.92, 0.48);
    animation: splash 3s cubic-bezier(0.8, 0.2, 0.2, 0.8) forwards;
  }
}

@keyframes splash {
  0% {
    height: 0%;
  }
  50% {
    height: 100%;
  }
  100% {
    top: 0;

    height: 0%;
  }
}
.norm {
  opacity: 0;
  margin-top: 3%;
  transition: opacity 0.5s ease-in, margin-top 1s;
}

.norm.fade {
  opacity: 1;
  margin-top: 0%;
}
</style>