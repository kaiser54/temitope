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
    const cursor = document.querySelector(".cursor");
    const innerCursor = document.querySelector(".inner-cursor");

    const followCursor = (e) => {
      const { clientX: x, clientY: y } = e;
      cursor.style.left = x + "px";
      cursor.style.top = y + "px";

      innerCursor.style.left = x + "px";
      innerCursor.style.top = y + "px";
    };

    // Remove the class after 5 seconds
    setTimeout(() => {
      this.isActive = false;
    }, 3500);

    window.addEventListener("mousemove", followCursor);
  },
  watch: {
    $route() {
      // Add the class when the route changes
      this.isActive = true;

      // Remove the class after 5 seconds
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
  /* position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  display: flex;
  justify-content: center;
  align-items: center; */

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

span {
  font-family: "Montserrat";
  text-transform: uppercase;
  font-weight: bold;
  font-size: 24px;
  color: #fff;
  letter-spacing: 2rem;
  /*   filter: blur(3px); */
  animation: blurMe 1.4s ease-in-out forwards;
  opacity: 0;
}

@for $i from 1 through 6 {
  span:nth-child(2n + #{$i}) {
    animation-delay: calc(2s + 200ms * #{$i});
  }
}

.cursor {
  position: fixed;
  transform: translate(-50%, -50%);
  border: 1px solid #fff;
  padding: 1rem;
  border-radius: 50%;
  pointer-events: none;
  mix-blend-mode: difference;
  opacity: 0;
  transition: transform 250ms ease, left 60ms linear, top 60ms linear;
}

.inner-cursor {
  position: fixed;
  transform: translate(-50%, -50%);
  background-color: #fff;
  padding: 1rem;
  border-radius: 50%;
  pointer-events: none;
  opacity: 0;
  mix-blend-mode: difference;
  transform-origin: center;
  transition: transform 250ms ease, left 60ms linear, top 60ms linear;
  animation: revealCursor 1s ease 5s forwards;
}

span:hover ~ .cursor {
  animation: blinkCursor 1s ease infinite;
  opacity: 1;
}

span:hover ~ .inner-cursor {
  transform: translate(-50%, -50%) scale(1.5);
}

@keyframes blinkCursor {
  0% {
    transform: translate(-50%, -50%) scale(1.5);
  }
  50% {
    transform: translate(-50%, -50%) scale(2.5);
  }
  100% {
    transform: translate(-50%, -50%) scale(1.5);
  }
}

@keyframes blurMe {
  0% {
    filter: blur(10px);
    opacity: 0;
  }
  100% {
    filter: blur(0px);
    opacity: 1;
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

@keyframes revealCursor {
  100% {
    opacity: 1;
  }
}
.norm {
  opacity: 0;
  transform: translateY(100%);
  transition: opacity .5s ease-in, transform 1.5s;
}

.norm.fade {
  opacity: 1;
  transform: translateY(0%);
}
</style>