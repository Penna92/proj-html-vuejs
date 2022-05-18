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

      <!-- ROW WITH 3 PHOTOS -->
      <div class="row my-5">
        <div
          class="col-12 col-md-6 col-lg-4 mb-3"
          v-for="card in sliderFirst"
          :key="card.index"
        >
          <AppSlider :item="card" />
        </div>
      </div>
      <!-- /ROW WITH 3 PHOTOS -->

      <!-- FEATURED ARTICLE -->
      <div id="featured-article" class="container-fluid text-white">
        <div class="container">
          <h6>FEATURED ARTICLE</h6>
          <h2>Cras malesuada et orci eget pharetra</h2>
          <p>
            In quis lectus sed leo elementum faucibus in dapibus dictum.
            Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at
            bibendum sadips ets ipsums dolores facilis uns leo lectus.
          </p>
          <button type="button" class="btn btn-dark">
            READ MORE <i class="fa-solid fa-angle-right"></i>
          </button>
        </div>
      </div>
      <!-- /FEATURED ARTICLE -->

      <!-- ROW WITH 3 PHOTOS -->
      <div class="row my-5">
        <div
          class="col-12 col-md-6 col-lg-4 mb-3"
          v-for="card in sliderSecond"
          :key="card.index"
        >
          <AppSlider :item="card" />
        </div>
      </div>
      <!-- /ROW WITH 3 PHOTOS -->

      <!-- ROW WITH 2 COLUMNS 2/3 - 1/3 -->
      <div class="row w-100">
        <!-- REVIEWED PRODUCT -->
        <div
          id="reviewed-product"
          class="
            container
            d-flex
            flex-column
            justify-content-center
            text-white
            col-sm-12 col-lg-8
            mb-3
          "
        >
          <h6>REVIEWED PRODUCT</h6>
          <h2>
            Mauris viverra atisan ipsum eget felis primis efficitur varius
          </h2>
          <p class="text-white">
            In quis lectus sed leo elementum faucibus in dapibus dictum.
            Nullamolestie tortor nec lectus venenatis, sed blandit dui, dolor at
            bibendum
          </p>
          <button type="button" class="btn btn-dark">
            <a
              href="https://avada.theme-fusion.com/forum/donec-ornare-pretium-eget-scelerisque-justo-commodo/"
              target="_blank"
              >READ MORE <i class="fa-solid fa-angle-right"></i
            ></a>
          </button>
        </div>
        <!-- REVIEWED PRODUCT -->

        <!-- TUTORIALS & GUIDES -->
        <aside id="tutorial-guides" class="container col-sm-12 col-lg-4 mb-3">
          <h2>Tutorials &#38; Guides</h2>
          <div class="orange-line"></div>
          <div class="d-flex flex-column justify-content-between">
            <div class="thumbnails row my-3">
              <div class="col-4">
                <img
                  class="img-fluid"
                  src="../assets/img/post_feat_img_23-147x118.jpg"
                  alt="Smartwatch thumbnail"
                />
              </div>
              <div class="col-8">
                <h5>Donec oranare pretium eget scelisque justo</h5>
                <p class="article-date">October 11th, 2015 | Comments Off</p>
              </div>
            </div>
            <div class="thumbnails row my-3">
              <div class="col-4">
                <img
                  class="img-fluid"
                  src="../assets/img/post_feat_img_22-147x118.jpg"
                  alt="Smartwatch thumbnail"
                />
              </div>
              <div class="col-8">
                <h5>Donec oranare pretium eget scelisque justo</h5>
                <p class="article-date">October 11th, 2015 | Comments off</p>
              </div>
            </div>
            <div class="thumbnails row my-3">
              <div class="col-4">
                <img
                  class="img-fluid"
                  src="../assets/img/post_feat_img_20-147x118.jpg"
                  alt="Smartwatch thumbnail"
                />
              </div>
              <div class="col-8">
                <h5>Donec oranare pretium eget scelisque justo</h5>
                <p class="article-date">October 11th, 2015 | Comments off</p>
              </div>
            </div>
          </div>
        </aside>
        <!-- /TUTORIALS & GUIDES -->
      </div>
      <!-- /ROW WITH 2 COLUMNS 2/3 - 1/3 -->
    </section>
    <!-- /LATEST NEWS SECTION -->
  </div>
</template>

<script>
import AppSlider from "../components/AppSlider.vue";
export default {
  name: "AppMain",
  components: {
    AppSlider,
  },
  data() {
    return {
      sliderFirst: [
        {
          image: "post_feat_img_25-700x441",
          title: "Morbi vitae dui euismod volputate sollicitudin",
          date: "October 11th, 2015 |",
          commentsNumber: "2 Comments",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
        {
          image: "post_feat_img_24-700x441",
          title: "Vivamus pellenteque, felis quis varius",
          date: "October 11th, 2015 |",
          commentsNumber: "Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
        {
          image: "post_feat_img_23-700x441",
          title: "Donec ornare pretium eget scelisque justo",
          date: "October 11th, 2015 |",
          commentsNumber: "Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
      ],

      sliderSecond: [
        {
          image: "post_feat_img_22-700x441",
          title: "Morbi vitae dui euismod volputate sollicitudin",
          date: "October 11th, 2015 |",
          commentsNumber: "Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
        {
          image: "post_feat_img_21-700x441",
          title: "Vivamus pellenteque, felis quis varius",
          date: "October 11th, 2015 |",
          commentsNumber: "Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
        {
          image: "post_feat_img_20-700x441",
          title: "Donec ornare pretium eget scelisque justo",
          date: "October 11th, 2015 |",
          commentsNumber: "Comments Off",
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla, vestibulum placerat metus mattis. Aenean dictum vitae nisl",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
button {
  background-color: black;
  width: 200px;
}
// DATA ARTICOLI
.article-date {
  font-size: 12px;
  color: $cape-cod;
}
//LINEA DI SEPARAZIONE ARANCIONE
.orange-line {
  height: 20px;
  width: 100px;
  border-bottom: 3px solid $salmon;
}
h6 {
  color: $cape-cod;
  font-size: 12px;
  font-weight: 700;
}
h5 {
  font-size: 16px;
  font-weight: 900;
  cursor: pointer;
  &:hover {
    color: $eastern-blue;
  }
}
h2 {
  font-weight: 900;
}
p {
  color: $cape-cod;
}
// SEZIONE A TUTTO SCHERMO SOTTO IL JUMBOTRON
#jumbotron-sub-section {
  background-color: $silver-chalice;
}
// SEZIONE FEATURED-ARTICLE
#featured-article {
  background: url("../assets/img/featured_article_1_bg.jpg") center center
    no-repeat;
  background-size: cover;
  .container {
    margin-top: 200px;
    margin-bottom: 150px;
    h6 {
      color: white;
    }
    p {
      color: $white;
    }
  }
}
// SEZIONE REVIEWED PRODUCT
#reviewed-product {
  background: url("../assets/img/featured_article_2_bg.jpg") center center
    no-repeat;
  background-size: cover;
  border-right: 20px solid white; //alternativa utile in certi casi per creare dei margini senza sballare flex.
  h6 {
    color: white;
  }
}
</style>