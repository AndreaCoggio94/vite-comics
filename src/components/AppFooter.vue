<script>
export default {
  data() {
    return {
      webPages: [
        "characters",
        "comics",
        "movies",
        "tv",
        "games",
        "collectibles",
        "videos",
        "fans",
        "news",
        "shop",
      ],
    };
  },
};
</script>

<template>
  <div class="top-footer">
    <div class="container d-flex">
      <ul>
        <li v-for="item in webPages">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.top-footer {
  color: white;
  background-image: url("/img/footer-bg.jpg");
}
</style>
