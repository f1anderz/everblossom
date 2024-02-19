<script>
import Trait from "@/components/AboutUsBlock/Trait.vue";

export default {
  name: "TraitsSection",
  components: {Trait},
  props: {
    traits: {
      type: Object,
      required: true
    }
  }
}
</script>

<template>
  <div class="about-us-traits">
    <div class="about-us-traits-header" v-html="this.traits.header"></div>
    <div class="about-us-traits-body">
      <transition-group name="traits">
        <trait v-for="trait in this.traits.items" :trait="trait" :key="trait.id"/>
      </transition-group>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.about-us-traits {
  display: flex;
  flex-direction: column;

  @include style.breakpoint(xs) {
    gap: .3rem;
    width: 85%;
    padding-top: 3vh;
  }

  @include style.breakpoint(s) {
    gap: .3rem;
    width: 85%;
  }

  @include style.breakpoint(m) {
    gap: .1rem;
    width: 85%;
  }

  @include style.breakpoint(l) {
    gap: .3rem;
    width: 85%;
  }

  @include style.breakpoint(xl) {
    gap: .3rem;
    width: 85%;
  }

  @include style.breakpoint(xxl) {
    gap: .6rem;
    width: 65%;
    padding-top: 5vh;
  }

  @include style.breakpoint(xxxl) {
    gap: 1.2rem;
    width: 65%;
    padding-top: 5vh;
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
      font-size: 1.5rem;
    }

    @include style.breakpoint(xl) {
      font-size: 1.6rem;
    }

    @include style.breakpoint(xxl) {
      font-size: 1.6rem;
    }

    @include style.breakpoint(xxxl) {
      font-size: 3.2rem;
    }
  }

  &-body {

    @include style.breakpoint(xs) {
      padding-left: 1rem;
    }

    @include style.breakpoint(s) {
      padding-left: 1rem;
    }

    @include style.breakpoint(m) {
      padding-left: 1rem;
    }

    @include style.breakpoint(l) {
      padding-left: 1.5rem;
    }

    @include style.breakpoint(xl) {
      padding-left: 1.8rem;
    }

    @include style.breakpoint(xxl) {
      padding-left: 2.5rem;
    }

    @include style.breakpoint(xxxl) {
      padding-left: 5rem;
    }
  }
}
</style>