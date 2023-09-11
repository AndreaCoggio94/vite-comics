<script>
export default {
  data() {
    return {};
  },
  props: {
    webPages: Array,
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
        <span
          :class="item.active ? 'active' : ''"
          class="text-uppercase"
          v-for="(item, index) in webPages"
          :key="index"
          href="#"
        >
          {{ item.text }}</span
        >
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
.nav-bar {
  background-color: white;
  font-size: 0.8rem;
  .container {
    justify-content: space-between;
    align-items: center;
    height: 7rem;

    .active {
      color: #0282f9;
    }
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
