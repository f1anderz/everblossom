<script>
export default {
  name: "Navigation",
  data() {
    return {
      menuActive: false
    }
  }
}
</script>

<template>
  <div class="navigation">
    <div class="navigation-links" :class="{shown: menuActive}">
      <div class="navigation-links-link"><a href="#about-us">About Us</a></div>
      <div class="navigation-links-link"><a href="#">Plants</a></div>
      <div class="navigation-links-link"><a href="#">Services</a></div>
      <div class="navigation-links-link"><a href="#">Feedback</a></div>
      <div class="navigation-links-link"><a href="#">Our works</a></div>
      <div class="navigation-links-link"><a href="#">Wholesale</a></div>
      <div class="navigation-links-link"><a href="#">Contacts</a></div>
    </div>
    <div class="navigation-menu" @click="this.menuActive = !this.menuActive;" :class="{rotated: menuActive}">
      <img src="@/assets/img/menu.svg" alt="Menu">
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.navigation {
  position: relative;
  display: flex;
  flex-direction: row;

  &-menu {
    padding-right: .4em;
    padding-top: .4em;

    & img {
      @include style.breakpoint(xs) {
        width: 1.5em;
        height: 1.5em;
        transition: transform .3s ease;
      }
    }
  }

  &-links {

    @include style.breakpoint(xs) {
      position: absolute;
      right: 0;
      width: 10em;
      display: flex;
      flex-direction: column;
      border-radius: 1em;
      padding-top: 1.5em;
      transform: translateX(100%);
      transition: transform .3s ease;
    }

    @include style.breakpoint(s) {
      display: flex;
      flex-direction: row;
    }

    @include style.breakpoint(m) {
      display: flex;
      flex-direction: row;
    }

    @include style.breakpoint(l) {
      display: flex;
      flex-direction: row;
    }

    @include style.breakpoint(xl){
      display: flex;
      flex-direction: row;
    }

    @include style.breakpoint(xxl) {
      display: flex;
      flex-direction: row;
    }

    @include style.breakpoint(xxxl){
      display: flex;
      flex-direction: row;
    }

    &-link {
      position: relative;

      @include style.breakpoint(xs) {
        font-size: 1.2em;
        padding: .5em 1.3em;

        &:last-child {
          border: none;
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
        }
      }

      @include style.breakpoint(s) {
        font-size: .8em;
        padding: 0 .5em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
          overflow: hidden;
        }
      }

      @include style.breakpoint(m) {
        font-size: .8em;
        padding: 0 .4em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
          overflow: hidden;
        }
      }

      @include style.breakpoint(l) {
        font-size: .9em;
        padding: 0 .6em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
          overflow: hidden;
        }
      }

      @include style.breakpoint(xl) {
        font-size: .9em;
        padding: 0 1em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
        }

        & a {
          position: relative;
          color: style.$text-color;
          text-decoration: none;
          overflow: hidden;
        }
      }

      @include style.breakpoint(xxl) {
        font-size: 1.2em;
        padding: 0 1.3em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
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

      @include style.breakpoint(xxxl) {
        font-size: 2.2em;
        padding: 0 1.3em;

        &:after {
          content: '';
          position: absolute;
          width: 1px;
          height: 1.2em;
          left: 100%;
          background-color: style.$text-color;
        }

        &:last-of-type {
          &:after {
            content: none;
          }
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
}

.rotated {
  & img {
    transform: rotate(-90deg);
  }
}

.shown {
  transform: translateX(0);
  background: style.$highlight-color;
}
</style>