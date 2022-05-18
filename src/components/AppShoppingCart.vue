<template>
  <a
    href="https://themeforest.net/item/avada-responsive-multipurpose-theme/2833226?irgwc=1&#38;clickid=V8GTRTVGixyIUnxSIMxN7w-dUkD0L43ZkTBxzc0&#38;iradid=275988&#38;irpid=1292887&#38;iradtype=ONLINE_TRACKING_LINK&#38;irmptype=mediapartner&#38;mp_value1=&#38;utm_campaign=af_impact_radius_1292887&#38;utm_medium=affiliate&#38;utm_source=impact_radius"
    id="shopping-cart"
  >
    <i id="visible-icon" class="fa-solid fa-cart-plus"></i>
    <i id="invisible-icon" class="fa-solid fa-cart-plus"></i>
    <span>Buy Now</span>
  </a>
</template>

<script>
export default {
  name: "AppShoppingCart",
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
#shopping-cart {
  position: fixed;
  top: 150px;
  right: 20px;
  height: 70px;
  width: 70px;
  border-radius: 5px;
  background-color: white;
  box-shadow: 0 10px 20px 5px rgb(0 0 0 / 15%);
  text-align: center;
  overflow: hidden;
  &:hover {
    #visible-icon {
      transform: translateX(-60px);
    }
    #invisible-icon {
      transform: translateX(-60px);
    }
  }
  #visible-icon {
    position: absolute;
    top: 13px;
    left: 50%;
    transform: translate(-50%);
    font-size: 20px;
    color: $cape-cod;
    transition: opacity 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      width 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      height 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      transform 0.2s cubic-bezier(0.21, 0.6, 0.35, 1);
  }
  #invisible-icon {
    font-size: 20px;
    color: $cape-cod;
    position: absolute;
    top: 13px;
    right: -35px;
    transition: opacity 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      width 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      height 0.4s cubic-bezier(0.21, 0.6, 0.35, 1),
      transform 0.2s cubic-bezier(0.21, 0.6, 0.35, 1);
  }
  span {
    position: absolute;
    left: 50%;
    transform: translate(-50%);
    bottom: 10px;
    font-size: 10px;
    color: $cape-cod;
    font-weight: bold;
    width: 100%;
  }
}
</style>