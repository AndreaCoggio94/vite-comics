<script>
export default {
  data() {
    return {};
  },
  props: {
    footerListComics: Array,
    footerListDC: Array,
    footerListShop: Array,
    footerListSites: Array,
  },
};
</script>

<template>
  <div class="top-footer">
    <div class="container d-flex">
      <ul>
        <h1>DC COMICS</h1>
        <li v-for="(item, index) in footerListComics" :key="index">
          {{ item }}
        </li>
      </ul>
      <ul>
        <h1>SHOP</h1>
        <li v-for="(item, index) in footerListShop" :key="index">
          {{ item }}
        </li>
      </ul>
      <ul>
        <h1>DC</h1>
        <li v-for="(item, index) in footerListDC" :key="index">
          {{ item }}
        </li>
      </ul>
      <ul>
        <h1>SITES</h1>
        <li v-for="(item, index) in footerListSites" :key="index">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
  <footer class="bottom-footer">
    <div class="container d-flex">
      <div class="col signUpButton">SIGN-UP NOW!</div>
      <div class="col-3 d-flex links">
        <h2>FOLLOW US</h2>
        <img src="/img/footer-facebook.png" alt="" />
        <img src="/img/footer-twitter.png" alt="" />
        <img src="/img/footer-youtube.png" alt="" />
        <img src="/img/footer-pinterest.png" alt="" />
        <img src="/img/footer-periscope.png" alt="" />
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.top-footer {
  color: white;
  background-image: url("/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  .container {
    max-height: 400px;
    flex-direction: column;
    flex-wrap: wrap;
    ul {
      list-style: none;
      padding: 0;
    }
  }
}
</style>
