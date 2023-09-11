<script>
export default {
  data() {
    return {
      buyPart: [
        {
          img: "/public/img/buy-comics-digital-comics.png",
          title: "digital comics",
        },
        {
          img: "/public/img/buy-comics-digital-comics.png",
          title: "digital comics",
        },
        {
          img: "/public/img/buy-comics-digital-comics.png",
          title: "digital comics",
        },
        {
          img: "/public/img/buy-comics-digital-comics.png",
          title: "digital comics",
        },
        {
          img: "/public/img/buy-comics-digital-comics.png",
          title: "digital comics",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="buy">
    <div class="container d-flex">
      <div class="d-flex" v-for="item in buyPart">
        <img :src="item.img" alt="" />
        <span> {{ item.title }} </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
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
