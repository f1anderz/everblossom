<script>
import TraitsSection from "@/components/AboutUsBlock/TraitsSection.vue";
import AboutUsSection from "@/components/AboutUsBlock/AboutUsSection.vue";

export default {
  name: "AboutUs",
  components: {AboutUsSection, TraitsSection},
  data() {
    return {
      aboutUsInfo: [
        {
          id: 1,
          name: "intro",
          image: "about-us-1",
          header: "Welcome to <span class='highlight'>everblossom</span>!",
          body: "At <span class='highlight'>everblossom</span>, we believe in the transformative power of nature's beauty. Established with a " +
              "passion for bringing the enchantment of greenery into every space, <span class='highlight'>everblossom</span> is your go-to " +
              "destination for premium decorative plants."
        },
        {
          id: 2,
          name: "story",
          image: "about-us-2",
          header: "Our Story:",
          body: "Founded in 2021, <span class='highlight'>everblossom</span> was born out of a shared love for botanical wonders and a vision to elevate " +
              "interior and exterior spaces with the timeless beauty of nature. What started as a humble endeavor has " +
              "now blossomed into a thriving hub for wholesale decorative plants."
        },
        {
          id: 3,
          name: "mission",
          image: "about-us-3",
          header: "Our Mission:",
          body: "At the core of our mission is the commitment to provide businesses with not just plants but living " +
              "works of art. We strive to curate a collection that goes beyond aesthetics, promoting wellness, " +
              "inspiration, and a harmonious connection with nature."
        }
      ],
      traits: {
        header: "What Sets Us <span class='highlight'>Apart</span>:",
        items: [
          {
            id: 1,
            header: "<span class='highlight'>Quality</span> Assurance:",
            body: "Each plant in our collection undergoes rigorous quality checks to ensure it meets our standards " +
                "of excellence."
          },
          {
            id: 2,
            header: "Unique <span class='highlight'>Selection</span>:",
            body: "Our curated assortment features a diverse range of plants, from exotic blooms to elegant foliage, " +
                "catering to various tastes and preferences."
          },
          {
            id: 3,
            header: "<span class='highlight'>Sustainability</span>:",
            body: "everblossom is dedicated to environmentally conscious practices, sourcing our plants responsibly " +
                "to reduce our ecological footprint."
          }
        ]
      }
    }
  }
}
</script>

<template>
  <div class="about-us-block" id="about-us">
    <transition-group name="about-us-info">
      <about-us-section v-for="info in this.aboutUsInfo" :section="info" :key="info.id"/>
    </transition-group>
    <traits-section class="about-us-block-traits" :traits="this.traits"/>
  </div>
</template>

<style scoped lang="scss">
@use '@/assets/scss/style';

.about-us-block {
  background-color: style.$background-color;
  overflow: hidden;
  display: flex;
  flex-direction: column;

  @include style.breakpoint(xs) {
    padding-bottom: 2rem;
    gap: 1.5rem;
    align-items: center;
  }

  @include style.breakpoint(s) {
    padding-bottom: 2rem;
    gap: 1.2rem;
    align-items: center;
  }

  @include style.breakpoint(m) {
    padding-bottom: 1rem;
    gap: 1rem;
    align-items: center;
  }

  @include style.breakpoint(l) {
    padding-bottom: 2rem;
    gap: 1.5rem;
    align-items: center;
  }

  @include style.breakpoint(xl) {
    padding-bottom: 2rem;
    gap: 1.8rem;
    align-items: center;
  }

  @include style.breakpoint(xxl) {
    padding-top: 8rem;
    padding-bottom: 8rem;
    gap: 7rem;
  }

  @include style.breakpoint(xxxl) {
    padding-top: 16rem;
    padding-bottom: 16rem;
    gap: 14rem;
  }

  &-intro {

    @include style.breakpoint(xxl) {
      margin-left: 18%;
    }

    @include style.breakpoint(xxxl) {
      margin-left: 18%;
    }
  }

  &-story {

    @include style.breakpoint(xxl) {
      margin-left: auto;
      margin-right: 6%;
    }

    @include style.breakpoint(xxxl) {
      margin-left: auto;
      margin-right: 6%;
    }
  }

  &-mission {

    @include style.breakpoint(xxl) {
      margin-left: 15%;
    }

    @include style.breakpoint(xxxl) {
      margin-left: 15%;
    }
  }

  &-traits {
    margin: 0 auto;
  }
}
</style>