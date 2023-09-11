<script>
export default {
  props: {
    thumb: String,
    series: String,
  },
};
</script>

<template>
  <div class="comic-card">
    <div class="image">
      <img class="" :src="thumb" alt="" />
    </div>
    <span class="">{{ series }}</span>
  </div>
</template>

<style lang="scss" scoped>
.comic-card {
  display: flex;
  flex-direction: column;
  width: 15%;
  margin: 0.25rem;
  text-align: center;
  font-size: 0.6rem;

  .image {
    height: 140px;
    aspect-ratio: 1;
    overflow: hidden;
    img {
      max-width: 100%;
    }
  }
}
</style>
