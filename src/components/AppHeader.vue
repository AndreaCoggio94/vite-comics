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
  <!-- nav-bar -->

  <nav class="nav-bar">
    <div class="container d-flex">
      <div class="col-4">
        <img src="/img/dc-logo.png" alt="logo.png" />
      </div>
      <div class="d-flex col">
        <span v-for="item in webPages" href="#"> {{ item }}</span>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.nav-bar {
  background-color: white;
  .container {
    justify-content: space-between;
    align-items: center;
    height: 7rem;
    .col-4 {
      display: flex;

      img {
        width: 5rem;
        aspect-ratio: 1;
      }
    }
    div.d-flex {
      justify-content: space-around;
    }
  }
}
</style>
