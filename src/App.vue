<script>
import AppFooter from "./components/AppFooter.vue";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
// import "bootstrap/dist/js/bootstrap.min.js";

export default {
  components: { AppHeader, AppMain, AppFooter },
};
</script>

<template>
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
// Import all of Bootstrap's CSS
@import "bootstrap/scss/bootstrap";
</style>
