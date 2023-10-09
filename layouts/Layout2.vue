<template>
  <div :class="{ animateContainer: isActive }" v-if="isActive">
    <!-- <span>T</span>
      <span>r</span>
      <span>a</span>
      <span>v</span>
      <span>e</span>
      <span>l</span> -->

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
  width: 100%;
  height: 100%;
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
  transform: translateY(3%);
  transition: opacity .5s ease-in, transform 1s;
}

.norm.fade {
  opacity: 1;
  transform: translateY(0%);
}
</style>