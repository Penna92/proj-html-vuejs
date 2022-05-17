<template>
  <section
    id="jumbotron"
    class="text-white d-flex justify-content-center align-items-center"
  >
    <!-- MAIN JUMBOTRON TITLE -->
    <div class="container">
      <h1>Tech Forum!</h1>
      <p>Discuss all the latest technology news and trends</p>
      <button type="button" class="btn text-white">
        GET AVADA NOW! <i class="fa-solid fa-angle-right"></i>
      </button>
    </div>
    <!-- /MAIN JUMBOTRON TITLE -->
  </section>
</template>

<script>
export default {
  name: "AppJumbotron",
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
#jumbotron {
  height: 100vh;
  background: url("../assets/img/home_slider_bg.jpg") center center no-repeat;
  background-size: cover;
  div.container {
    h1 {
      font-size: 120px;
      font-weight: 700;
    }
    button {
      background-color: $eastern-blue;
      font-weight: bold;
      width: 200px;
    }
  }
}
</style>