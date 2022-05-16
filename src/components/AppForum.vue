<template>
  <section class="text-center">
    <!-- READ OUR BLOG -->
    <div id="our-blog" class="text-center text-white">
      <h5>
        <span>READ OUR BLOG <i class="fa-solid fa-right-long"></i></span>
      </h5>
    </div>
    <!-- /READ OUR BLOG -->
    <!-- FORUM SECTIONS -->
    <section id="forum-section" class="d-flex flex-column align-items-center">
      <h6>PHASELLUS EGET METUS</h6>
      <h2>Forum Sections</h2>
      <div class="orange-line"></div>
      <!-- MAIN GRID -->
      <div class="container row d-flex justify-content-center gap-5 my-5">
        <div
          class="
            card
            d-flex
            flex-column
            justify-content-center
            align-items-center
            gap-3
          "
          v-for="(item, index) in cards.icons"
          :key="index"
        >
          <div class="orange-circle"><i :class="item"></i></div>
          <h5>{{ cards.titles[index] }}</h5>
        </div>
      </div>
      <!-- /MAIN GRID -->
    </section>
    <!-- /FORUM SECTIONS -->
  </section>
</template>

<script>
export default {
  name: "AppForum",
  data() {
    return {
      cards: {
        icons: [
          "fa-solid fa-file-lines",
          "fa-brands fa-apple",
          "fa-brands fa-windows",
          "fa-brands fa-android",
          "fa-solid fa-mug-saucer",
          "fa-solid fa-cubes",
          "fa-solid fa-laptop",
          "fa-solid fa-wrench",
        ],
        titles: [
          "News & Community",
          "Apple Forum",
          "Microsoft Forum",
          "Android Forum",
          "General Discussion",
          "Apps & Software",
          "Gadgets & Stuff",
          "Tutorials & Guides",
        ],
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/variables.scss";
#our-blog {
  height: 100px;
  background-color: black;
  h5 {
    line-height: 100px;
    span {
      cursor: pointer;
    }
  }
}
#forum-section {
  background-color: $silver-chalice;
  padding: 50px 0;
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
  .card {
    width: 250px;
    height: 250px;
    border-top: 5px solid $eastern-blue;
    .orange-circle {
      width: 70px;
      height: 70px;
      line-height: 70px;
      border-radius: 50%;
      background-color: $salmon;
      i {
        font-size: 32px;
        color: white;
      }
    }
    h5 {
      font-weight: 900;
    }
  }
}
</style>