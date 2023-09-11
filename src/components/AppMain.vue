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
    <div class="container">
      <div class="btn-blue">CURRENT SERIES</div>
      <div class="d-flex">
        <AppCards
          comics
          v-for="(comic, index) in comics"
          :key="index"
          :thumb="comic.thumb"
          :series="comic.series"
        />
      </div>
      <div class="btn btn-blue">LOAD MORE</div>
    </div>
  </div>

  <div class="buy">
    <div class="container d-flex">
      <div class="d-flex" v-for="(item, index) in buyCards" :key="index">
        <img :src="item.img" alt="" />
        <span class="text-uppercase"> {{ item.title }} </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.jumbotron {
  background-image: linear-gradient(rgba(0, 0, 0, 0) 300px, rgb(0, 0, 0) 300px),
    url("/img/jumbotron.jpg");
  padding-top: 280px;
  background-repeat: no-repeat;
  background-size: contain;
  .container {
    display: flex;
    flex-direction: column;
    .btn-blue {
      color: white;
      background-color: blue;
      display: inline-block;
      padding: 0.5rem 1rem;
      margin: 0 auto 0 0;
    }
    .btn-blue.btn {
      align-self: center;
      margin: auto;
      border-radius: 0;
    }
    .d-flex {
      flex-wrap: wrap;
      padding: 1rem 0.25rem;
      justify-content: space-around;
      color: white;
    }
  }
}

.buy {
  background-color: rgb(71, 71, 223);
  color: white;
  .container {
    padding: 2rem 0;
    justify-content: space-around;
    font-size: 0.8rem;
    div.d-flex {
      align-items: center;
      justify-content: space-around;
      img {
        width: 2.5rem;
        margin-right: 0.5rem;
      }
    }
  }
}
</style>
