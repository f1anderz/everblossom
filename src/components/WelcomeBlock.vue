<script>
export default {
  name: "Welcome",
  data() {
    return {
      prevScrollPos: 0
    }
  },
  methods: {
    imageFlow(event) {
      let images = document.querySelectorAll('.welcome-block-main-image');
      let scrollPos = window.scrollY;

      this.prevScrollPos = scrollPos;
    }
  },
  mounted() {
    document.addEventListener('scroll', this.imageFlow);
  }
}
</script>

<template>
  <div class="welcome-block" id="welcome" @scroll="this.imageFlow">
    <img class="welcome-block-wave" src="@/assets/img/wave.svg" alt="wave">
    <div class="welcome-block-header">
      <div class="welcome-block-header-container">
        <div class="welcome-block-header-container-icon"><img src="@/assets/img/favicon.webp" alt="Icon"></div>
        <div class="welcome-block-header-container-title"><a href="#welcome">everblossom</a></div>
      </div>
      <div class="welcome-block-header-nav">
        <div class="welcome-block-header-nav-link"><a href="#about-us">About Us</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Plants</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Services</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Feedback</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Our works</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Wholesale</a></div>
        <div class="welcome-block-header-nav-link"><a href="#">Contacts</a></div>
      </div>
    </div>
    <div class="welcome-block-main">
      <div class="welcome-block-main-slogan">Unveiling Beauty, One Leaf at a Time — <span
          class="highlight">everblossom</span></div>
      <div class="welcome-block-main-introduction">Welcome to <span class="highlight">everblossom</span> — your
        destination for premium decorative
        plants that redefine elegance and bring a touch of nature into every space. Discover a curated collection of
        botanical wonders, each carefully selected to enhance the beauty of your surroundings. From exquisite blooms to
        lush foliage, our passion for quality and design is evident in every leaf. Explore our best plants and
        embark on a journey to transform your spaces with the timeless allure of nature. Elevate your surroundings with
        <span class="highlight">everblossom</span> — where beauty blossoms, and elegance flourishes.
      </div>
      <img class="welcome-block-main-image" style="z-index: 3; top: 10%; left: 110%;"
           src="@/assets/img/gardening-background.webp" alt="Plants">
      <img class="welcome-block-main-image" style=" top: 60%; left: 150%;" src="@/assets/img/seedlings-dark.webp"
           alt="Plants">
      <img class="welcome-block-main-image" style="top: -35%; left: 140%;" src="@/assets/img/closeup-plant.webp"
           alt="Plants">
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.welcome-block {
  position: relative;
  height: 100vh;
  display: flex;
  flex-direction: column;
  gap: 25vh;
  overflow: hidden;
  background-color: style.$background-color;

  &-header {
    position: relative;
    z-index: 3;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    color: style.$text-color;
    font-family: style.$font-header;
    padding: 1em;

    &-container {
      display: flex;
      flex-direction: row;
      align-items: center;
      gap: 1em;

      &-icon {
        & img {
          width: 4em;
          height: 4em;
          user-select: none;
          pointer-events: none;
        }
      }

      &-title {
        font-size: 2em;

        & a {
          color: style.$text-color;
          text-decoration: none;
        }
      }
    }

    &-nav {
      display: flex;
      flex-direction: row;

      &-link {
        font-size: 1.2em;
        padding: 0 1.3em;
        border-right: 1px solid style.$text-color;

        &:last-child {
          border: none;
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
          overflow: hidden;

          &:before {
            content: '';
            position: absolute;
            left: 50%;
            top: 100%;
            transform: translate(-50%, -50%);
            width: 0;
            height: 1px;
            background-color: style.$highlight-color;
            transition: all 0.5s ease;
          }

          &:hover {
            color: style.$highlight-color;

            &:before {
              width: 100%;
              left: 0;
              transform: translate(0, -50%);
            }
          }
        }
      }
    }
  }

  &-main {
    position: relative;
    font-family: style.$font-body;
    color: style.$text-color;
    width: 35%;
    margin-left: 15%;
    padding: 1.2em;
    border-radius: 1em;
    text-align: center;

    &-slogan {
      font-size: 2.3em;
    }

    &-introduction {
      font-size: 1.2em;
    }

    &-image {
      position: absolute;
      display: block;
      width: 25em;
      height: 25em;
      border-radius: 50%;
      overflow: hidden;

      &:hover {
        opacity: .95;
      }
    }
  }

  &-wave {
    position: absolute;
    z-index: 2;
    display: block;
    transform: scaleX(1.7);
    opacity: .9;
    pointer-events: none;
  }
}

@keyframes wave-animation {
  0%, 100% {
    transform: scaleX(2) translateX(-25%);
  }
  50% {
    transform: scaleX(2) translateX(25%);
  }
}
</style>