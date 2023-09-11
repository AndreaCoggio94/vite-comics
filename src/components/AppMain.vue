<script>
import AppCards from "./AppCards.vue";

export default {
  data() {
    return {};
  },
  components: {
    AppCards,
  },
  props: {
    buyCards: Array,
    comics: Array,
  },
};
</script>

<template>
  <!-- content goes here -->

  <div class="jumbotron">
    <div class="container d-flex">
      <AppCards
        comics
        v-for="(comic, index) in comics"
        :key="index"
        :thumb="comic.thumb"
        :series="comic.series"
      />
    </div>
  </div>

  <div class="buy">
    <div class="container d-flex">
      <div class="d-flex" v-for="(item, index) in buyCards" :key="index">
        <img :src="item.img" alt="" />
        <span> {{ item.title }} </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.jumbotron {
  .container {
    flex-wrap: wrap;
    // align-items:
    justify-content: space-around;
    color: white;
  }
}

.buy {
  background-color: rgb(71, 71, 223);
  color: white;
  .container {
    min-height: 10rem;
    justify-content: space-around;

    div.d-flex {
      align-items: center;
      justify-content: space-around;
      img {
        width: 3rem;
        margin-right: 0.5rem;
      }
    }
  }
}
</style>
