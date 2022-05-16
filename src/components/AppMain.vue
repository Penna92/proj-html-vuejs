<template>
  <div id="main">
    <!-- JUMBOTRON GREY SUB-SECTION -->
    <section
      id="jumbotron-sub-section"
      class="d-flex justify-content-center align-items-center"
    >
      <div
        class="
          d-flex
          flex-column
          justify-content-center
          align-items-center
          text-center
          my-5
        "
      >
        <h6>AVADA FORUM IS THE PLACE TO BE</h6>
        <p>
          In quis lectus sed leo elementum faucibus in dapibus dictum. <br />
          Nulla Molestie torto nec lectus venenatis, sed blandit dui finibus.
          <br />
          dolor at, bibendum purus, Donec vehicula nec torto ac finibus.
        </p>
      </div>
    </section>
    <!-- /JUMBOTRON GREY SUB-SECTION -->

    <!-- LATEST NEWS SECTION -->
    <section
      id="latest-news"
      class="
        container
        d-flex
        flex-column
        justify-content-center
        align-items-center
        my-5
      "
    >
      <h6>PHASELLUS EGET METUS</h6>
      <h2>All the latest news</h2>
      <div class="orange-line"></div>
      <div class="row my-5">
        <div class="col-12 col-md-6 col-lg-4 mb-3">
          <img
            class="img-fluid"
            src="../assets/img/post_feat_img_25-700x441.jpg"
            alt="Smartphone-1"
          />
          <h5 class="mt-3">Morbi vitae dui euismod volputate sollicitudin</h5>
          <p class="article-date">
            October 11th,2015 |
            <span style="color: black; font-weight: bold">2 Comments</span>
          </p>
          <p>
            Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut
            erat fringilla, vestibulum placerat metus mattis. Aenean dictum
            vitae nisl.
          </p>
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-3">
          <img
            class="img-fluid"
            src="../assets/img/post_feat_img_24-700x441.jpg"
            alt="Smartphone-2"
          />
          <h5 class="mt-3">Morbi vitae dui euismod volputate sollicitudin</h5>
          <p class="article-date">October 11th,2015 | Comments off</p>
          <p>
            Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut
            erat fringilla, vestibulum placerat metus mattis. Aenean dictum
            vitae nisl.
          </p>
        </div>
        <div class="col-12 col-md-6 col-lg-4 mb-3">
          <img
            class="img-fluid"
            src="../assets/img/post_feat_img_23-700x441.jpg"
            alt="Smartwatch-3"
          />
          <h5 class="mt-3">Morbi vitae dui euismod volputate sollicitudin</h5>
          <p class="article-date">October 11th,2015 | Comments off</p>
          <p>
            Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut
            erat fringilla, vestibulum placerat metus mattis. Aenean dictum
            vitae nisl.
          </p>
        </div>
      </div>
    </section>
    <!-- /LATEST NEWS SECTION -->
  </div>
</template>

<script>
export default {
  name: "AppMain",
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/styles/variables.scss";
.article-date {
  font-size: 12px;
}
.orange-line {
  height: 20px;
  width: 100px;
  border-bottom: 3px solid $salmon;
}
h6 {
  font-size: 12px;
  font-weight: 700;
}
h5 {
  font-size: 16px;
  font-weight: 900;
}
h2 {
  font-weight: 900;
}
p {
  color: $cape-cod;
}
#jumbotron-sub-section {
  background-color: $silver-chalice;
}
</style>