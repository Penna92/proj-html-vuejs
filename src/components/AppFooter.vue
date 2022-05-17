<template>
  <section id="footer">
    <!-- PARTE SUPERIORE DEL FOOTER CON LISTE DI LINK -->
    <div
      id="top-footer"
      class="d-flex justify-content-center align-items-center my-5"
    >
      <section id="footer-links" class="container row">
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
          <li><h4>AVADA TECH FORUM</h4></li>
          <p class="my-3">
            Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis
            auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi
            sit amet mi intermentum.
          </p>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
          <li><h4>POPULAR TOPICS</h4></li>
          <li v-for="(link, index) in popularTopics" :key="index" class="my-3">
            <a href="" class="d-flex align-items-"> {{ link }}</a>
            <hr />
          </li>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
          <li><h4>RECENT POSTS</h4></li>
          <li v-for="(link, index) in recentPosts" :key="index" class="my-3">
            <a href=""> {{ link }}</a>
            <hr />
          </li>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-3">
          <li><h4>LATEST REPLIES</h4></li>
          <li v-for="(link, index) in latestReplies" :key="index" class="my-3">
            <a href=""> {{ link }}</a>
            <hr />
          </li>
        </ul>
      </section>
    </div>
    <!-- /PARTE SUPERIORE DEL FOOTER CON LISTE DI LINK -->

    <!-- PARTE INFERIORE DEL FOOTER CON COPYRIGHT E ICONE SOCIAL -->
    <div
      id="bottom-footer"
      class="container mb-5 d-flex justify-content-between align-items-center"
    >
      <span>
        © Copyright 2012 - 2022 | Avada Theme by <a href="">ThemeFusion</a> |
        All Rights Reserved | Powered by
        <a href="https://github.com/Penna92" target="_blank">Penna92</a>
      </span>
      <div id="social-icons" class="d-flex gap-3">
        <div id="facebook" class="icon-circle">
          <a href=""><i class="fa-brands fa-facebook-f"></i></a>
        </div>
        <div id="twitter" class="icon-circle">
          <a href=""><i class="fa-brands fa-twitter"></i></a>
        </div>
        <div id="instagram" class="icon-circle">
          <a href=""><i class="fa-brands fa-instagram"></i></a>
        </div>
        <div id="youtube" class="icon-circle">
          <a href=""><i class="fa-brands fa-youtube"></i></a>
        </div>
      </div>
    </div>
    <!-- PARTE /INFERIORE DEL FOOTER CON COPYRIGHT E ICONE SOCIAL -->
  </section>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      popularTopics: [
        "Morbi vitae dui euismod vulputate sollicitudin",
        "Vivamus pellenteque, felis quis varius",
        "Donec ornare pretium eget scelisque justo",
      ],
      recentPosts: [
        "Morbi vitae dui euismod vulputate sollicitudin",
        "Vivamus pellenteque, felis quis varius",
        "Donec ornare pretium eget scelisque justo",
      ],
      latestReplies: [
        "Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin",
        "Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin",
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../assets/styles/variables.scss";
#top-footer {
  border-bottom: 1px solid #eaeaea;
  #footer-links {
    ul {
      padding: 30px;
      p {
        color: $cape-cod;
        height: 100%;
      }
      li {
        list-style-type: none;
        h4 {
          margin-bottom: 50px;
        }
        a {
          text-decoration: none;
          color: black;
          height: 100%;
          &:hover {
            color: $eastern-blue !important;
          }
          &::before {
            position: absolute;
            content: "›";
            margin-left: -10px;
          }
        }
      }
    }
  }
}
#bottom-footer {
  span {
    color: $cape-cod;
    a {
      text-decoration: none;
      font-weight: bold;
      color: black;
      &:hover {
        color: $eastern-blue !important;
      }
    }
  }
  #social-icons {
    .icon-circle {
      text-align: center;
      height: 50px;
      line-height: 50px;
      width: 50px;
      border-radius: 50%;
      background-color: blue;
      transition: transform 0.3s;
      cursor: pointer;
      &:hover {
        transform: scale(1.2);
        background-color: $salmon !important;
      }
      a {
        text-decoration: none;
        color: white;
      }
    }
    #facebook {
      background-color: $san-marino-vibrant;
    }
    #twitter {
      background-color: $boston-blue;
    }
    #instagram {
      background-color: $wedgewood;
    }
    #youtube {
      background-color: $totem-pole;
    }
  }
}
</style>