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
        <a
          href="https://themeforest.net/item/avada-responsive-multipurpose-theme/2833226?irgwc=1&#38;clickid=V8GTRTVGixyIUnxSIMxN7w-dUkD0LDWdkTBxzc0&#38;iradid=275988&#38;irpid=1292887&#38;iradtype=ONLINE_TRACKING_LINK&#38;irmptype=mediapartner&#38;mp_value1=&#38;utm_campaign=af_impact_radius_1292887&#38;utm_medium=affiliate&#38;utm_source=impact_radius"
          target="_blank"
          >GET AVADA NOW! <i class="fa-solid fa-angle-right"></i
        ></a>
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