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
      <div class="container row d-flex justify-content-between gap-5 my-5">
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

    <!-- GO TO OUR FORUM -->
    <div id="our-forum" class="text-center text-white">
      <h5>
        <span>GO TO OUR FORUM <i class="fa-solid fa-right-long"></i></span>
      </h5>
    </div>
    <!-- /GO TO OUR FORUM -->

    <!-- COMMUNITY HERO -->
    <div id="community-hero" class="d-flex justify-content-center text-white">
      <div class="wrapper">
        <h2>
          Hey! Join to our <br />
          Community
        </h2>
        <p class="my-3">
          Nulla molestie torto nec lectus venenatis, sed blandit dui finibus.
          Curabitur feugiat vulputate purus ipsums dolore ficilis uns etra.
        </p>
        <button type="button" class="btn text-white">
          SIGN UP <i class="fa-solid fa-angle-right"></i>
        </button>
      </div>
    </div>
    <!-- /COMMUNITY HERO -->
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
#our-blog,
#our-forum {
  height: 100px;
  background-color: black;
  cursor: pointer;
  &:hover {
    background-color: $eastern-blue;
  }
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
    color: $cape-cod;
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
    cursor: pointer;
    &:hover {
      h5 {
        color: $salmon;
        transform: scale(1.2);
      }
      .orange-circle {
        transform: scale(1.2);
        box-shadow: 0px 0px 10px 2px $salmon;
        // box-shadow: 0px 2px 2px 2px $salmon;
        border: 3px solid white;
      }
    }
    .orange-circle {
      transition: transform 0.2s;
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
      transition: transform 0.3s;
      font-weight: 900;
    }
  }
}
#community-hero {
  background: url("../assets/img/join_now_cta_bg.jpg") center center no-repeat;
  background-size: cover;
  .wrapper {
    width: 50%;
    padding: 100px 0;
    h2 {
      font-weight: 900;
    }
    button {
      background-color: $eastern-blue;
      font-weight: bold;
      width: 200px;
    }
  }
}
</style>