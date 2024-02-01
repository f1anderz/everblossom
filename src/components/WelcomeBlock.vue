<script>
import Navigation from "@/components/WelcomeBlock/Navigation.vue";

export default {
  name: "Welcome",
  components: {Navigation}
}
</script>

<template>
  <div class="welcome-block" id="welcome">
    <img class="welcome-block-wave" src="@/assets/img/wave.svg" alt="wave">
    <div class="welcome-block-header">
      <div class="welcome-block-header-container">
        <div class="welcome-block-header-container-icon"><img src="@/assets/img/favicon.webp" alt="Icon"></div>
        <div class="welcome-block-header-container-title"><a href="#welcome">everblossom</a></div>
      </div>
      <navigation/>
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
      <img class="welcome-block-main-image"
           src="@/assets/img/gardening-background.webp" alt="Plants">
      <img class="welcome-block-main-image" src="@/assets/img/seedlings-dark.webp"
           alt="Plants">
      <img class="welcome-block-main-image" src="@/assets/img/closeup-plant.webp"
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
  overflow: hidden;
  background-color: style.$background-color;

  @include style.breakpoint(xs) {
    gap: 5vh;
  }

  @include style.breakpoint(s) {
    gap: 7vh;
  }

  @include style.breakpoint(m) {
    gap: 10vh;
  }

  @include style.breakpoint(l) {
    gap: 20vh;
  }

  @include style.breakpoint(xl) {
  }

  @include style.breakpoint(xxl) {
    gap: 25vh;
  }

  @include style.breakpoint(xxxl) {

  }

  &-header {
    position: relative;
    z-index: 3;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    color: style.$text-color;
    font-family: style.$font-header;

    @include style.breakpoint(xs) {
      padding: .1em .6em;
    }

    @include style.breakpoint(s) {
      padding: .1em .4em;
    }

    @include style.breakpoint(m) {
      padding: .1em .6em;
    }

    @include style.breakpoint(l) {
    }

    @include style.breakpoint(xl) {
    }

    @include style.breakpoint(xxl) {
      padding: 1em;
    }

    @include style.breakpoint(xxxl) {

    }

    &-container {
      display: flex;
      flex-direction: row;
      align-items: center;

      @include style.breakpoint(xs) {
        gap: .2em;
      }

      @include style.breakpoint(s) {
        gap: .2em;
      }

      @include style.breakpoint(m) {
        gap: .3em;
      }

      @include style.breakpoint(l) {
        gap: .3em;
      }

      @include style.breakpoint(xl) {

      }

      @include style.breakpoint(xxl) {
        gap: .5em;

      }

      @include style.breakpoint(xxxl) {

      }

      &-icon {
        & img {
          user-select: none;
          pointer-events: none;

          @include style.breakpoint(xs) {
            width: 2em;
            height: 2em;
          }

          @include style.breakpoint(s) {
            width: 2.5em;
            height: 2.5em;
          }

          @include style.breakpoint(m) {
            width: 3.5em;
            height: 3.5em;
          }

          @include style.breakpoint(l) {
            width: 3.5em;
            height: 3.5em;
          }

          @include style.breakpoint(xl) {

          }

          @include style.breakpoint(xxl) {
            width: 4em;
            height: 4em;
          }

          @include style.breakpoint(xxxl) {

          }
        }
      }

      &-title {

        @include style.breakpoint(xs) {
          font-size: 1.3em;
        }

        @include style.breakpoint(s) {
          font-size: 1.4em;
        }

        @include style.breakpoint(m) {
          font-size: 1.4em;
        }

        @include style.breakpoint(l) {
          font-size: 1.5em;
        }

        @include style.breakpoint(xl) {

        }

        @include style.breakpoint(xxl) {
          font-size: 2em;
        }

        @include style.breakpoint(xxxl) {

        }

        & a {
          color: style.$text-color;
          text-decoration: none;
        }
      }
    }
  }

  &-main {
    position: relative;
    display: flex;
    flex-direction: column;
    font-family: style.$font-body;
    color: style.$text-color;
    text-align: center;

    @include style.breakpoint(xs) {
      width: 90%;
      margin: 0 auto;
      padding: .5em;
    }

    @include style.breakpoint(s) {
      width: 55%;
      margin-left: 5%;
    }

    @include style.breakpoint(m) {
      width: 90%;
      margin: 0 auto;
      gap: .5em;
    }

    @include style.breakpoint(l) {
      width: 50%;
      margin-left: 5%;
    }

    @include style.breakpoint(xl) {

    }

    @include style.breakpoint(xxl) {
      width: 35%;
      margin-left: 15%;
      padding: 1.2em;
      gap: 1em;
    }

    @include style.breakpoint(xxxl) {

    }

    &-slogan {

      @include style.breakpoint(xs) {
        font-size: 1.4em;
      }

      @include style.breakpoint(s) {
        font-size: 1.3em;
      }

      @include style.breakpoint(m) {
        font-size: 1.5em;
      }

      @include style.breakpoint(l) {
        font-size: 1.7em;
      }

      @include style.breakpoint(xl) {

      }

      @include style.breakpoint(xxl) {
        font-size: 2.1em;
      }

      @include style.breakpoint(xxxl) {

      }
    }

    &-introduction {

      @include style.breakpoint(xs) {
        font-size: .9em;
      }

      @include style.breakpoint(s) {
        font-size: .9em;
      }

      @include style.breakpoint(m) {
        font-size: 1.1em;
      }

      @include style.breakpoint(l) {
        font-size: 1.1em;
      }

      @include style.breakpoint(xl) {
      }

      @include style.breakpoint(xxl) {
        font-size: 1.2em;
      }

      @include style.breakpoint(xxxl) {

      }
    }

    &-image {
      position: absolute;
      display: block;
      border-radius: 50%;
      overflow: hidden;

      @include style.breakpoint(xs) {
        width: 9em;
        height: 9em;
        top: 108%;
        left: 60%;

        &:first-of-type {
          z-index: 3;
          top: 113%;
          left: 0;
        }

        &:last-of-type {
          top: 123%;
          left: 30%;
        }
      }

      @include style.breakpoint(s) {
        width: 9em;
        height: 9em;
        top: 48%;
        left: 128%;

        &:first-of-type {
          z-index: 3;
          top: 28%;
          left: 106%;
        }

        &:last-of-type {
          top: 3%;
          left: 125%;
        }
      }

      @include style.breakpoint(m) {
        width: 18em;
        height: 18em;
        top: 125%;
        left: 60%;

        &:first-of-type {
          z-index: 3;
          top: 130%;
          left: 0;
        }

        &:last-of-type {
          top: 160%;
          left: 30%;
        }
      }

      @include style.breakpoint(l) {
        width: 15em;
        height: 15em;
        top: 51%;
        left: 134%;

        &:first-of-type {
          z-index: 3;
          top: 28%;
          left: 106%;
        }

        &:last-of-type {
          top: -3%;
          left: 130%;
        }
      }

      @include style.breakpoint(xl) {

      }

      @include style.breakpoint(xxl) {
        width: 25em;
        height: 25em;
        top: 40%;
        left: 150%;

        &:first-of-type {
          z-index: 3;
          top: 10%;
          left: 110%;
        }

        &:last-of-type {
          top: -30%;
          left: 140%;
        }
      }

      @include style.breakpoint(xxxl) {

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

    @include style.breakpoint(xs) {
      height: 5.5em;
    }

    @include style.breakpoint(s) {
      height: 6.5em;
    }

    @include style.breakpoint(m) {
      height: 7em;
    }

    @include style.breakpoint(l) {

    }

    @include style.breakpoint(xl) {
    }

    @include style.breakpoint(xxl) {

    }

    @include style.breakpoint(xxxl) {

    }
  }
}
</style>