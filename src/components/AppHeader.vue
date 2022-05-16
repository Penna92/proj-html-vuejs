<template>
  <div id="header">
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
        <ul class="d-flex">
          <li v-for="(link, index) in headerLinks" :key="index" class="mx-3">
            {{ link }} <i class="fa-solid fa-caret-down"></i>
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
      font-weight: bold;
      background-color: black;
    }
  }
}
</style>
