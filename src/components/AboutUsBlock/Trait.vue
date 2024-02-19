<script>
export default {
  name: "Trait",
  props: {
    trait: {
      type: Object,
      required: true
    }
  }
}
</script>

<template>
  <div class="about-us-trait">
    <div class="about-us-trait-header" v-html="this.trait.header"></div>
    <div class="about-us-trait-body">{{ this.trait.body }}</div>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.about-us-trait {
  display: flex;
  flex-direction: column;
  gap: .1rem;

  &-header {
    font-family: style.$font-header;

    @include style.breakpoint(xs) {
      font-size: 1.2rem;
    }

    @include style.breakpoint(m) {
      font-size: 1.3rem;
    }

    @include style.breakpoint(l) {
      font-size: 1.4rem;
    }

    @include style.breakpoint(xl) {
      font-size: 1.5rem;
    }

    @include style.breakpoint(xxl) {
      font-size: 1.4rem;
    }

    @include style.breakpoint(xxxl) {
      font-size: 2.8rem;
    }
  }

  &-body {
    font-family: style.$font-body;

    @include style.breakpoint(xs) {
      padding-left: 1rem;
    }

    @include style.breakpoint(s) {
      font-size: .8em;
      padding-left: 1rem;
    }

    @include style.breakpoint(m) {
      font-size: 1.1em;
      padding-left: 1rem;
    }

    @include style.breakpoint(l) {
      font-size: 1.2em;
      padding-left: 1rem;
    }

    @include style.breakpoint(xl) {
      font-size: 1.3em;
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
</style>