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
          <input type="checkbox" />
          <span class="menu"> <span class="hamburger"></span> </span>
          <ul>
            <li v-for="(link, index) in headerLinks" :key="index">
              <a href="#">{{ link }}</a>
            </li>
            <button type="button" class="btn btn-dark">JOIN US</button>
            <i class="fa-solid fa-magnifying-glass ms-3"></i>
          </ul>
        </label>
        <!-- /HAMBURGER MENU -->
        <ul id="navbar-ul" class="d-flex">
          <li v-for="(link, index) in headerLinks" :key="index" class="mx-3">
            <a href="">{{ link }}</a> <i class="fa-solid fa-caret-down"></i>
          </li>
        </ul>
        <button type="button" class="btn btn-dark">JOIN US</button>
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
      // NAVBAR LINKS ARRAY
      headerLinks: [
        "Home",
        "Apple",
        "Microsoft",
        "Android",
        "Forums",
        "Contact us",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
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
          font-size: 30px;
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
    }
    .fa-magnifying-glass {
      cursor: pointer;
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
  h1 {
    position: absolute;
    top: 50%;
    left: 50%;
    -webkit-transform: translate(-50%, -50%);
    transform: translate(-50%, -50%);
    width: 80%;
    text-align: center;
  }
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
  margin-bottom: 1em;
  display: block;
  color: #f38630;
  text-decoration: none;
}

// MEDIA QUERIES
@media screen and (min-width: 992px) {
  label {
    display: none;
  }
}

@media screen and (max-width: 992px) {
  #navbar-ul li {
    display: none;
  }
  // nav button {
  //   display: none;
  // }
  nav i {
    display: none;
  }
  label ul li a {
    color: $eastern-blue !important;
  }
}
</style>
