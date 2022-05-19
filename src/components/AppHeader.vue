<template>
  <div id="header" class="d-flex align-items-center">
    <div
      class="
        d-flex
        container
        align-items-center
        justify-content-between
        text-white
      "
    >
      <!-- LOGO -->
      <div id="header-logo" class="d-flex align-items-center">
        <img src="../assets/img/logo.png" alt="Logo" />
      </div>
      <!-- /LOGO -->
      <!-- NAVBAR -->
      <nav class="d-flex align-items-center">
        <!-- HAMBURGER MENU -->
        <label>
          <input @click="clickedMenu = !clickedMenu" type="checkbox" />
          <span class="menu">
            <span class="hamburger"></span>
          </span>
          <ul v-if="clickedMenu === true" class="d-flex flex-column">
            <li v-for="(link, index) in headerLinks" :key="index">
              <a :href="link.landingPage" target="_blank">{{ link.name }}</a>
            </li>
            <li>
              <button type="button" class="btn btn-dark">
                <a
                  href="https://avada.theme-fusion.com/forum/join/"
                  target="_blank"
                  >JOIN US</a
                >
              </button>
            </li>
          </ul>
        </label>
        <!-- /HAMBURGER MENU -->
        <ul id="navbar-ul" class="d-flex">
          <li v-for="(link, index) in headerLinks" :key="index" class="mx-3">
            <a :href="link.landingPage" target="_blank">{{ link.name }}</a>
            <i class="fa-solid fa-caret-down"></i>
          </li>
        </ul>
        <button type="button" class="btn btn-dark">
          <a href="https://avada.theme-fusion.com/forum/join/" target="_blank"
            >JOIN US</a
          >
        </button>
        <i class="fa-solid fa-magnifying-glass ms-3"></i>
      </nav>
      <!-- /NAVBAR -->
    </div>
  </div>
</template>

<script>
export default {
  name: "AppHeader",
  data() {
    return {
      clickedMenu: false,
      // NAVBAR LINKS ARRAY
      headerLinks: [
        {
          name: "Home",
          landingPage: "https://avada.theme-fusion.com/forum/",
        },
        {
          name: "Apple",
          landingPage: "https://avada.theme-fusion.com/forum/apple/",
        },
        {
          name: "Microsoft",
          landingPage: "https://avada.theme-fusion.com/forum/microsoft/",
        },
        {
          name: "Android",
          landingPage: "https://avada.theme-fusion.com/forum/android/",
        },
        {
          name: "Forums",
          landingPage: "https://avada.theme-fusion.com/forum/forums/",
        },
        {
          name: "Contact us",
          landingPage: "https://avada.theme-fusion.com/forum/contact-us/",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
#header-logo {
  img {
    cursor: pointer;
    transition: 1s;
    transform: scale(1);
    &:hover {
      transform: scale(0.9);
    }
  }
}
#header {
  position: fixed;
  left: 0;
  top: 0;
  right: 0;
  height: 100px;
  background-color: $eastern-blue;
  z-index: 999;
  nav {
    height: 100%;
    line-height: 100px;
    ul {
      height: 100%;
      margin-bottom: 0 !important;
      li {
        position: relative;
        height: 100%;
        list-style-type: none;
        cursor: pointer;
        &:hover {
          i {
            display: block;
            z-index: 999999;
          }
          a {
            color: white;
          }
        }
        a {
          text-decoration: none;
          color: #afe1e9;
        }
        i {
          font-size: 40px;
          position: absolute;
          bottom: 0;
          color: $eastern-blue;
          right: 50%;
          transform: translate(50%, 50%);
          display: none;
        }
      }
    }
    button {
      background-color: black;
      a {
        display: block;
        width: 100%;
        height: 100%;
        text-decoration: none;
        color: white;
        font-weight: bold;
      }
    }
    .fa-magnifying-glass {
      cursor: pointer;
      color: #afe1e9;
      &:hover {
        color: white;
      }
    }
  }
}

// HAMBURGER MENU
*,
*:before,
*:after {
  box-sizing: border-box;
}

label .menu {
  position: absolute;
  right: -100px;
  top: -100px;
  z-index: 100;
  width: 200px;
  height: 200px;
  background: #fff;
  border-radius: 50% 50% 50% 50%;
  -webkit-transition: 0.5s ease-in-out;
  transition: 0.5s ease-in-out;
  box-shadow: 0 0 0 0 #fff, 0 0 0 0 #fff;
  cursor: pointer;
}

label .hamburger {
  position: absolute;
  top: 135px;
  left: 50px;
  width: 30px;
  height: 2px;
  background: #69d2e7;
  display: block;
  -webkit-transform-origin: center;
  transform-origin: center;
  -webkit-transition: 0.5s ease-in-out;
  transition: 0.5s ease-in-out;
}

label .hamburger:after,
label .hamburger:before {
  -webkit-transition: 0.5s ease-in-out;
  transition: 0.5s ease-in-out;
  content: "";
  position: absolute;
  display: block;
  width: 100%;
  height: 100%;
  background: $eastern-blue;
}

label .hamburger:before {
  top: -10px;
}

label .hamburger:after {
  bottom: -10px;
}

label input {
  display: none;
}

label input:checked + .menu {
  box-shadow: 0 0 0 100vw #fff, 0 0 0 100vh #fff;
  border-radius: 0;
}

label input:checked + .menu .hamburger {
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
}

label input:checked + .menu .hamburger:after {
  -webkit-transform: rotate(90deg);
  transform: rotate(90deg);
  bottom: 0;
}

label input:checked + .menu .hamburger:before {
  -webkit-transform: rotate(90deg);
  transform: rotate(90deg);
  top: 0;
}

label input:checked + .menu + ul {
  opacity: 1;
}

label ul {
  z-index: 200;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  opacity: 0;
  -webkit-transition: 0.25s 0s ease-in-out;
  transition: 0.25s 0s ease-in-out;
}

label a {
  display: block;
  text-decoration: none;
}

// MEDIA QUERIES
@media screen and (min-width: 992px) {
  label {
    display: none;
  }
}

@media screen and (max-width: 991px) {
  #header nav {
    line-height: 50px;
  }
  #navbar-ul {
    display: none;
  }
  #navbar-ul li {
    display: none;
  }
  nav button {
    display: none;
  }
  nav i {
    display: none;
  }
  label ul {
    position: fixed;
    display: flex !important;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    // background-color: white;
    overflow-y: auto;
    -webkit-animation: smooth 1s ease-in;
    -moz-animation: smooth 1s ease-in;
    -o-animation: smooth 1s ease-in;
    -ms-animation: smooth 1s ease-in;
    animation: smooth 1s ease-in;
  }
  @keyframes smooth {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }
  label ul li a {
    color: $eastern-blue !important;
    height: 100% !important;
  }
  label ul li {
    height: 50px !important;
  }
  label button {
    display: flex;
    align-items: center;
    align-content: center;
  }
  label ul li i {
    color: $eastern-blue !important;
    display: block;
    z-index: 9999;
  }
}
</style>
