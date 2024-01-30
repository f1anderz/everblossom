<script>
import AboutUs from "@/components/AboutUsBlock.vue";
import Contacts from "@/components/ContactsBlock.vue";
import DoneDeals from "@/components/DoneDealsBlock.vue";
import Services from "@/components/ServicesBlock.vue";
import Showcase from "@/components/ShowcaseBlock.vue";
import Testimonials from "@/components/TestimonialsBlock.vue";
import Welcome from "@/components/WelcomeBlock.vue";
import WholesaleInfo from "@/components/WholesaleInformationBlock.vue";

export default {
  name: "App",
  components: {
    AboutUs,
    Contacts,
    DoneDeals,
    Services,
    Showcase,
    Testimonials,
    Welcome,
    WholesaleInfo
  }
}
</script>

<template>
  <div class="wrapper">
    <welcome/>
    <about-us/>
    <showcase/>
    <services/>
    <testimonials/>
    <done-deals/>
    <wholesale-info/>
    <contacts/>
  </div>
</template>

<style lang="scss">
@use '@/assets/scss/style';
</style>
