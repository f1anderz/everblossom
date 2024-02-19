<script>
export default {
  name: "AboutUsSection",
  props: {
    section: {
      type: Object,
      required: true
    }
  }
}
</script>

<template>
  <div class="about-us-section" :class="'about-us-block-' + this.section.name">
    <div class="about-us-section-info">
      <div class="about-us-section-info-header" v-html="this.section.header"></div>
      <div class="about-us-section-info-body" v-html="this.section.body"></div>
    </div>
    <img :src="'./src/assets/img/' + this.section.image + '.webp'" :alt="this.section.img">
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.about-us-section {
  position: relative;
  display: flex;
  flex-direction: column;

  @include style.breakpoint(xs) {
    width: 96%;
    gap: 1rem;
  }

  @include style.breakpoint(s) {
    width: 96%;
    gap: 1rem;
  }

  @include style.breakpoint(m) {
    width: 96%;
    gap: 1rem;
  }

  @include style.breakpoint(l) {
    width: 95%;
    gap: 1.5rem;
  }

  @include style.breakpoint(xl) {
    width: 93%;
    gap: 1.8rem;
  }

  @include style.breakpoint(xxl) {
    width: 65%;
  }

  @include style.breakpoint(xxxl) {
    width: 65%;
  }

  &-info {
    display: flex;
    flex-direction: column;
    gap: .2rem;

    @include style.breakpoint(xs) {
      width: 80%;
    }

    @include style.breakpoint(s) {
      width: 90%;
    }

    @include style.breakpoint(m) {
      width: 90%;
    }

    @include style.breakpoint(l) {
      width: 90%;
    }

    @include style.breakpoint(xl) {
      width: 90%;
    }

    @include style.breakpoint(xxl) {
      width: 40%;
    }

    @include style.breakpoint(xxxl) {
      width: 40%;
    }

    &-header {
      font-family: style.$font-header;

      @include style.breakpoint(xs) {
        font-size: 1.2rem;
      }

      @include style.breakpoint(s) {
        font-size: 1.1rem;
      }

      @include style.breakpoint(m) {
        font-size: 1.4rem;
      }

      @include style.breakpoint(l) {
        font-size: 1.3rem;
      }

      @include style.breakpoint(xl) {
        font-size: 1.4rem;
      }

      @include style.breakpoint(xxl) {
        font-size: 1.6rem;
      }

      @include style.breakpoint(xxxl) {
        font-size: 3.2rem;
      }
    }

    &-body {
      font-family: style.$font-body;

      @include style.breakpoint(xs) {
        padding-left: 1rem;
      }

      @include style.breakpoint(s) {
        font-size: .8rem;
        padding-left: 1rem;
      }

      @include style.breakpoint(m) {
        font-size: 1.1em;
        padding-left: 1rem;
      }

      @include style.breakpoint(l) {
        font-size: 1.2rem;
        padding-left: 1rem;
      }

      @include style.breakpoint(xl) {
        font-size: 1.3rem;
        padding-left: 1rem;
      }

      @include style.breakpoint(xxl) {
        font-size: 1.2rem;
        padding-left: 2rem;
      }

      @include style.breakpoint(xxxl) {
        font-size: 2.4rem;
        padding-left: 4rem;
      }
    }
  }

  & img {
    display: block;
    border-radius: .1rem;

    @include style.breakpoint(s) {
      width: 98%;
      margin-left: 2%;
    }

    @include style.breakpoint(xxl) {
      position: absolute;
      width: 40%;
      left: 55%;
      top: -50%;
    }

    @include style.breakpoint(xxxl) {
      position: absolute;
      width: 40%;
      left: 55%;
      top: -50%;
    }
  }
}
</style>