<template>
  <Layout2>
    <div class="wrapper">
      <div class="hero">
        <header>
          <div class="hero-content">
            <div class="machina">FRONT-</div>
            <div class="ma-sa">
              <div class="sans">
                "I take pride in engineering <br />
                robust and scalable frontend solutions <br />
                that offer exceptional user experiences."
              </div>
              <div class="machina">END</div>
            </div>
            <div class="machina">DEVELOPER</div>
          </div>
        </header>

        <section>
          <div class="content-wrap reveal-on-scroll" ref="revealElement">
            <p class="sans">
              Hi, My name is Agboola Temitope Oluwasegun, a dedicated senior
              Frontend Developer currently at
              <a href="https://app.ipc-africa.com/">IPC-Africa</a> with a
              passion for crafting exceptional user experiences. I specialize in
              translating design concepts into responsive, interactive, and
              visually stunning websites.
            </p>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 104.11 93.95">
              <defs class="svg-proprty"></defs>
              <g id="Layer_2" data-name="Layer 2">
                <g id="Layer_1-2" data-name="Layer 1">
                  <circle class="cls-1" cx="57.14" cy="46.98" r="46.48" />
                  <circle class="cls-1" cx="46.98" cy="46.98" r="46.48" />
                  <text class="cls-2" transform="translate(27.51 44.84)">
                    LE
                    <tspan class="cls-3" x="17.05" y="0">AR</tspan>
                    <tspan x="37.48" y="0">N</tspan>
                    <tspan class="cls-4" x="2.52" y="14">MO</tspan>
                    <tspan class="cls-5" x="27.81" y="14">R</tspan>
                    <tspan x="37.89" y="14">E</tspan>
                  </text>
                  <g class="cls-6">
                    <polyline
                      class="cls-1"
                      points="50.2 28.42 70.61 28.42 70.61 48.83"
                    />
                    <line
                      class="cls-1"
                      x1="70.61"
                      y1="28.42"
                      x2="33.5"
                      y2="65.53"
                    />
                  </g>
                </g>
              </g>
            </svg>
          </div>
          <div class="image slide-in-image" ref="imageElement"></div>
        </section>
        <div class="scroll-wrap reveal-on-scroll" ref="animateReveal">
          <div class="scroll-container">
            <div class="scroll-content">
              <span class="machina">AGBOOLA TEMITOPE OLUWASEGUN</span>
              <span class="machina">AGBOOLA TEMITOPE OLUWASEGUN</span>
              <span class="machina">AGBOOLA TEMITOPE OLUWASEGUN</span>
              <span class="machina">AGBOOLA TEMITOPE OLUWASEGUN</span>
            </div>
          </div>
        </div>
      </div>
      <main>
        <div class="hr"></div>
        <div class="header">
          <div class="title machina">SLILLS</div>
          <div class="snippet sans">
            Allow me to introduce my proficiency in the world of frontend
            development. I specialize in crafting immersive web experiences that
            captivate users, enhance their journeys, and extend the frontiers of
            the digital realm.
          </div>
        </div>
        <div class="reveal-on-scroll" ref="revealElement2">
          <div class="container">
            <div class="box" id="box1" style="animation-delay: 214.286ms"></div>
            <div class="box" id="box2" style="animation-delay: 428.571ms"></div>
            <div class="box" id="box3" style="animation-delay: 642.857ms"></div>
            <div class="box" id="box4" style="animation-delay: 857.143ms"></div>
            <div class="box" id="box5" style="animation-delay: 428.571ms"></div>
            <div class="box" id="box6" style="animation-delay: 642.857ms"></div>
            <div class="box" id="box7" style="animation-delay: 857.143ms"></div>
            <div class="box" id="box7" style="animation-delay: 1071.43ms"></div>
            <div class="box" id="box8" style="animation-delay: 642.857ms"></div>
            <div class="box" id="box9" style="animation-delay: 857.143ms"></div>
            <div class="box" id="box7" style="animation-delay: 1071.43ms"></div>
            <div class="box" id="box7" style="animation-delay: 1285.71ms"></div>
          </div>
        </div>
      </main>
      <main>
        <div class="hr"></div>
        <div class="header">
          <div class="title machina">PROJECTS</div>
          <div class="snippet sans">
            Below, you'll find a curated collection of projects that show my
            unwavering dedication to crafting captivating web journeys, and
            elevating user experiences
          </div>
        </div>
      </main>
    </div>
  </Layout2>
</template>

<script>
import Layout2 from "/layouts/Layout2.vue";
export default {
  components: { Layout2 },
  data() {
    return {};
  },
  mounted() {
    const options = {
      threshold: 0.5, // Adjust this value as needed
    };

    const revealObserver = new IntersectionObserver(
      this.handleRevealIntersection,
      options
    );
    revealObserver.observe(this.$refs.revealElement);

    const revealObserver2 = new IntersectionObserver(
      this.handleRevealIntersection2,
      options
    );
    revealObserver2.observe(this.$refs.revealElement2);

    const imageObserver = new IntersectionObserver(
      this.handleImageIntersection,
      options
    );
    imageObserver.observe(this.$refs.imageElement);

    const animateObserver = new IntersectionObserver(
      this.handleAnimateObserver,
      options
    );
    animateObserver.observe(this.$refs.animateReveal);
  },

  methods: {
    handleRevealIntersection(entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("reveal"); // Add the 'reveal' class when element is in view
        } else {
          entry.target.classList.remove("reveal"); // Remove the 'reveal' class when element is out of view
        }
      });
    },

    handleRevealIntersection2(entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("reveal"); // Add the 'reveal' class when element is in view
        } else {
          entry.target.classList.remove("reveal"); // Remove the 'reveal' class when element is out of view
        }
      });
    },

    handleImageIntersection(entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("slide"); // Add the 'slide' class when image is in view
        } else {
          entry.target.classList.remove("slide"); // Remove the 'slide' class when image is out of view
        }
      });
    },

    handleAnimateObserver(entries) {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("reveal"); // Add the 'slide' class when image is in view
        } else {
          entry.target.classList.remove("reveal"); // Remove the 'slide' class when image is out of view
        }
      });
    },
  },
};
</script>

<style lang="scss" scoped>
.machina {
  font-family: "Neue Machina";
}
.sans {
  font-family: "DM Sans";
}
.hero-content {
  height: 90vh;
  color: white;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  .machina {
    font-size: 92px;
    font-weight: 700;
    line-height: 93%;
  }
  .sans {
    font-size: 16px;
    line-height: 24px;
  }
  .ma-sa {
    display: flex;
    flex-direction: row;
    align-items: center;
    gap: 60px;
    .sans {
      max-width: 392px;
      text-transform: uppercase;
    }
  }
}
.scroll-wrap {
  position: relative;
  /* height: 100px; */
  margin-top: -170px;
  .scroll-container {
    overflow: hidden;
    white-space: nowrap;
    /* position: absolute; */
    z-index: 9;
    width: 100%;

    .scroll-content {
      display: inline-block;
      animation: scroll 80s linear infinite;
      font-size: 10rem;
      color: white;

      span {
        margin-right: 40px; /* Adjust the spacing between instances */
      }
    }
  }
}

@keyframes scroll {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-90%);
  }
}
section {
  display: flex;
  max-width: 90%;
  margin-inline: auto;
  justify-content: space-between;
  overflow: hidden;
  height: 100%;
  .content-wrap {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-start;
    p.sans {
      color: white;
      text-transform: uppercase;
      max-width: 400px;

      a {
        color: #00dc82;
        &:hover {
          text-decoration: underline;
        }
      }
    }
    svg {
      cursor: pointer;
      height: 20%;
      margin-bottom: 200px;
      fill: none;
      stroke: #fff;
      stroke-miterlimit: 10;
      transition: stroke 0.3s ease, transform 0.3s ease;
      .cls-1 {
        fill: none;
        stroke: #fff;
        stroke-miterlimit: 10;
      }
      .cls-2 {
        font-size: 15.64px;
        fill: #fff;
        font-family: NeueMachina-Light, Neue Machina;
        font-weight: 100;
        transition: opacity 0.3s ease;
      }
      .cls-3 {
        letter-spacing: -0.01em;
      }
      .cls-4 {
        letter-spacing: -0.02em;
      }
      .cls-5 {
        letter-spacing: -0.01em;
      }
      .cls-6 {
        opacity: 0;
        transition: opacity 0.3s ease, stroke 0.3s ease;
      }
    }
    svg:hover {
      transform: scale(0.5);
      .cls-2 {
        opacity: 0;
      }
      .cls-6 {
        opacity: 1;
      }
    }
  }
  .image {
    width: 40em;
    height: 40em;
    background: grey;
    border-radius: 5%;
  }
}

main {
  width: 100%;
  display: flex;
  flex-direction: column;
  margin-top: 200px;
  gap: 32px;
  .hr {
    height: 1px;
    background-color: #ffffff30;
    width: 90%;
    margin-inline: auto;
  }
  .header {
    width: 90%;
    margin-inline: auto;
    padding-bottom: 30px;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    .title {
      color: #fff;
    }
    .snippet {
      max-width: 30%;
      text-align: right;
    }
  }
}

/* assets/css/styles.css */
.reveal-on-scroll {
  opacity: 0;
  transform: translateY(20px); /* Initial hidden state */
  transition: opacity 0.5s ease, transform 0.5s ease;
}

.reveal-on-scroll.reveal {
  opacity: 1;
  transform: translateY(0); /* Final revealed state */
}
/* assets/css/styles.css */
.slide-in-image {
  opacity: 0;
  transform: translateX(20%); /* Initial hidden state */
  transition: opacity 1s ease, transform 1s ease;
}
.slide-in-image.slide {
  opacity: 1;
  transform: translateX(0); /* Final revealed state */
}

.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 30px;
  width: 70%;
  margin: 0 auto;

  .box {
    border-radius: 20px;
    width: 100%;
    height: 100px;
    background-color: #3498db;
    background: linear-gradient(
      120deg,
      #5c589f 4.89%,
      #58559c 50%,
      #25244d 102%
    );
    opacity: 0;
    animation: scale-in 1s cubic-bezier(0.22, 1, 0.36, 1) infinite alternate;
    animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.2);

    &:nth-child(4),
    &:nth-child(9) {
      visibility: hidden;
    }
  }
}

@keyframes scale-in {
  0% {
    opacity: 0;
    transform: scale(0.4);
  }

  100% {
    opacity: 1;
    transform: scale(1);
  }
}
</style>