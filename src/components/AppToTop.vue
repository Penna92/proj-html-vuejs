<template>
  <div id="toTop">
    <a href="#"><i class="fa-solid fa-angle-up"></i></a>
  </div>
</template>

<script>
export default {
  name: "AppToTop",
};
</script>

<style lang="scss" >
@import "../assets/styles/variables.scss";
#toTop {
  background-color: #333;
  border-radius: 4px 4px 0 0;
  height: 30px;
  width: 50px;
  line-height: 30px;
  text-align: center;
  position: fixed;
  bottom: 0px;
  right: 10px;
  a {
    display: block;
    height: 100%;
    width: 100%;
    color: white;
  }
}
</style>