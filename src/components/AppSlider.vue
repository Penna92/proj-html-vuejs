<template>
  <div>
    <div>
      <a :href="item.landingPage" target="_blank">
        <img
          class="img-fluid"
          :src="require('../assets/img/' + item.image + '.jpg')"
          alt="Tablet-1"
        />
      </a>
    </div>
    <a :href="item.landingPage" target="_blank">
      <h5 class="mt-3">{{ item.title }}</h5>
    </a>
    <p class="article-date">
      {{ item.date }}
      <span :class="{ hasComments: item.commentsNumber !== 'Comments Off' }">{{
        item.commentsNumber
      }}</span>
    </p>
    <p>
      {{ item.text }}
    </p>
  </div>
</template>

<script>
export default {
  name: "AppSlider",
  props: ["item"],
};
</script>

<style scoped lang="scss">
@import "../assets/styles/variables.scss";
p {
  color: $cape-cod;
}
h5 {
  color: black;
  font-size: 16px;
  font-weight: 900;
  cursor: pointer;
  &:hover {
    color: $eastern-blue;
  }
}
.hasComments {
  color: black;
  cursor: pointer;
  &:hover {
    color: $eastern-blue;
  }
}
</style>