<template>
  <div id="app">
      <app-header></app-header>
      <app-welcome></app-welcome>
      <app-about></app-about>
      <app-services></app-services>
      <app-recent-work></app-recent-work>
      <app-contact></app-contact>
      <app-footer></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Welcome from "./components/Welcome.vue";
import About from "./components/About.vue";
import Services from "./components/Services.vue";
import Contact from "./components/Contact.vue";
import RecentWork from "./components/RecentWork.vue";
import ServiceSingle from "./components/ServiceSingle.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    "app-header": Header,
    "app-welcome": Welcome,
    "app-services": Services,
    "app-contact": Contact,
    "app-recent-work": RecentWork,
    "app-about": About,
    "app-footer": Footer,
    "app-service-single": ServiceSingle
  },
  name: "app",
  data() {
    return {};
  }
};
</script>

<style>

</style>
