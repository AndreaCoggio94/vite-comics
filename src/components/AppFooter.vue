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
      <div class="links d-flex">
        <ul>
          <h1>DC COMICS</h1>
          <li
            class="text-capitalize"
            v-for="(item, index) in footerListComics"
            :key="index"
          >
            {{ item }}
          </li>
        </ul>
        <ul>
          <h1>SHOP</h1>
          <li
            class="text-capitalize"
            v-for="(item, index) in footerListShop"
            :key="index"
          >
            {{ item }}
          </li>
        </ul>
        <ul>
          <h1>DC</h1>
          <li
            class="text-capitalize"
            v-for="(item, index) in footerListDC"
            :key="index"
          >
            {{ item }}
          </li>
        </ul>
        <ul>
          <h1>SITES</h1>
          <li
            class="text-capitalize"
            v-for="(item, index) in footerListSites"
            :key="index"
          >
            {{ item }}
          </li>
        </ul>
      </div>
      <div class="logo d-flex">
        <img src="/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
  </div>
  <footer class="bottom-footer">
    <div class="container d-flex">
      <div class="signUp-button">SIGN-UP NOW!</div>
      <div class="col-5 d-flex links">
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
    width: 100%;
    height: 100%;
    justify-content: space-between;
    .links {
      max-height: 400px;
      flex-direction: column;
      flex-wrap: wrap;

      padding: 1rem 0;

      h1 {
        font-size: 1rem;
        padding-bottom: 1rem;
      }
      ul {
        list-style: none;
        padding: 0;
        li {
          font-size: 0.8rem;
          padding-right: 1rem;
        }
      }
    }

    .logo {
      overflow: hidden;
      max-height: 350px;
      align-items: center;
      justify-content: flex-end;

      img {
        width: 80%;
        aspect-ratio: 1;
      }
    }
  }
}

.bottom-footer {
  background-color: #303030;
  color: white;
  .container {
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
    .signUp-button {
      border: 2px solid #0282f9;
      padding: 0.5rem;
    }
    div.d-flex {
      justify-content: space-around;
      align-items: center;

      h2 {
        font-size: 1.5rem;
        padding-right: 0.5rem;
        color: #0282f9;
      }
      img {
        padding: 0 0.5rem;
        height: 2rem;
      }
    }
  }
}
</style>
