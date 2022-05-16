<template>
  <div id="app">
    <header>
      <AppHeader />
      <AppJumbotron />
    </header>
    <main>
      <AppMain />
      <AppForum />
      <AppNewsletter />
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
import AppForum from "./components/AppForum.vue";
import AppNewsletter from "./components/AppNewsletter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbotron,
    AppMain,
    AppFooter,
    AppForum,
    AppNewsletter,
  },
};
</script>

<style lang="scss">
@import "./assets/styles/general.scss";
</style>
