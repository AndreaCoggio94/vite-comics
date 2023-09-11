<script>
export default {
  data() {
    return {
      message: "La mia prima app con Vite!",
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
  <div class="container">
    <nav class="nav-bar d-flex">
      <div class="col-4">
        <img src="../../public/img/dc-logo.png" alt="logo.png" />
      </div>
      <div class="d-flex col">
        <span v-for="item in webPages" href="#"> {{ item }}</span>
      </div>
    </nav>
  </div>
</template>

<style lang="scss" scoped>
.nav-bar {
  justify-content: space-between;
  align-items: center;

  .col-4 {
    display: flex;
    align-items: center;
    justify-content: center;
    img {
      width: 5rem;
      aspect-ratio: 1;
    }
  }
  div.d-flex {
    justify-content: space-around;
  }
}
</style>
