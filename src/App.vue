<template>
  <div id="app">
    <header>
      <AppHeader />
      <AppJumbotron />
    </header>
    <main>
      <AppMain />
    </main>
    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";
import AppJumbotron from "./components/AppJumbotron.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbotron,
    AppMain,
    AppFooter,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/general.scss";
</style>
