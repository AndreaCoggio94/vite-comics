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
  <!-- nav-bar -->

  <nav class="nav-bar">
    <div class="container d-flex">
      <div class="col-4">
        <img src="../../public/img/dc-logo.png" alt="logo.png" />
      </div>
      <div class="d-flex col">
        <span v-for="item in webPages" href="#"> {{ item }}</span>
      </div>
    </div>
  </nav>

  <!-- content goes here -->

  <div class="jumbotron">
    <div class="container d-flex">
      <span> content goes here </span>
    </div>
  </div>
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

.jumbotron {
  .container {
    min-height: 8rem;
    align-items: center;
    justify-content: flex-start;
    color: white;
  }
}
</style>
