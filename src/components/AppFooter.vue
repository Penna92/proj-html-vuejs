<template>
  <section id="footer">
    <!-- PARTE SUPERIORE DEL FOOTER CON LISTE DI LINK -->
    <div
      id="top-footer"
      class="d-flex justify-content-center align-items-center my-5"
    >
      <section
        id="footer-links"
        class="container row d-flex justify-content-between"
      >
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-2">
          <li><h4>AVADA TECH FORUM</h4></li>
          <p class="my-3">
            Sed semper, nisl id feugiat eleifend, erat est digssim felis, quis
            auctor elit enim nec ante. Cras et nibh risus. Pellentesque non mi
            sit amet mi intermentum.
          </p>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-2">
          <li><h4>POPULAR TOPICS</h4></li>
          <li v-for="(link, index) in popularTopics" :key="index" class="my-3">
            <a :href="link.landingPage" target="_blank"> {{ link.title }}</a>
            <hr />
          </li>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-2">
          <li><h4>RECENT POSTS</h4></li>
          <li v-for="(link, index) in recentPosts" :key="index" class="my-3">
            <a :href="link.landingPage" target="_blank"> {{ link.title }}</a>
            <hr />
          </li>
        </ul>
        <ul class="col-xs-12 col-sm-6 col-md-4 col-lg-2">
          <li><h4>LATEST REPLIES</h4></li>
          <li v-for="(link, index) in latestReplies" :key="index" class="my-3">
            <a :href="link.landingPage" target="_blank"> {{ link.title }}</a>
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
        © Copyright 2012 - 2022 | Avada Theme by
        <a href="https://theme-fusion.com/" target="_blank">ThemeFusion</a> |
        All Rights Reserved | Powered by
        <a href="https://github.com/Penna92" target="_blank">Penna92</a>
      </span>
      <div id="social-icons" class="d-flex gap-3">
        <div id="facebook" class="icon-circle">
          <a href="https://www.facebook.com/ThemeFusionAvada/" target="_blank"
            ><i class="fa-brands fa-facebook-f"></i
          ></a>
        </div>
        <div id="twitter" class="icon-circle">
          <a href="https://twitter.com/theme_fusion" target="_blank"
            ><i class="fa-brands fa-twitter"></i
          ></a>
        </div>
        <div id="instagram" class="icon-circle">
          <a href="https://www.instagram.com/themefusion/" target="_blank"
            ><i class="fa-brands fa-instagram"></i
          ></a>
        </div>
        <div id="youtube" class="icon-circle">
          <a
            href="https://www.youtube.com/channel/UC_C7uAOAH9RMzZs-CKCZ62w"
            target="_blank"
            ><i class="fa-brands fa-youtube"></i
          ></a>
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
        {
          title: "Morbi vitae dui euismod vulputate sollicitudin",
          landingPage:
            "https://avada.theme-fusion.com/forum/morbi-vitae-dui-euismod-vulputate-sollicitudin/",
        },
        {
          title: "Vivamus pellenteque, felis quis varius",
          landingPage:
            "https://avada.theme-fusion.com/forum/vivamus-pellentesque-felis-quis-varius-hendrerit/",
        },
        {
          title: "Donec ornare pretium eget scelisque justo",
          landingPage:
            "https://avada.theme-fusion.com/forum/donec-ornare-pretium-eget-scelerisque-justo-commodo/",
        },
      ],
      recentPosts: [
        {
          title: "Morbi vitae dui euismod vulputate sollicitudin",
          landingPage:
            "https://avada.theme-fusion.com/forum/morbi-vitae-dui-euismod-vulputate-sollicitudin/",
        },
        {
          title: "Vivamus pellenteque, felis quis varius",
          landingPage:
            "https://avada.theme-fusion.com/forum/vivamus-pellentesque-felis-quis-varius-hendrerit/",
        },
        {
          title: "Donec ornare pretium eget scelisque justo",
          landingPage:
            "https://avada.theme-fusion.com/forum/donec-ornare-pretium-eget-scelerisque-justo-commodo/",
        },
      ],
      latestReplies: [
        {
          title:
            "Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin",
          landingPage:
            "https://avada.theme-fusion.com/forum/morbi-vitae-dui-euismod-vulputate-sollicitudin/#comment-3",
        },
        {
          title:
            "Dario Pineda on Morbi vitae dui euismod vulputate sollicitudin",
          landingPage:
            "https://avada.theme-fusion.com/forum/morbi-vitae-dui-euismod-vulputate-sollicitudin/#comment-2",
        },
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
      padding: 0;
      width: 280px;
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

@media screen and (max-width: 768px) {
  #social-icons {
    flex-direction: column;
  }
}
</style>