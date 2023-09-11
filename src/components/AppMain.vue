<script>
export default {
  data() {
    return {
      message: "La mia prima app con Vite!",
    };
  },
};
</script>

<template>
  <header>
    <h1>{{ message }}</h1>
  </header>
</template>

<style lang="scss" scoped>
h1 {
  font-size: 3rem;
}
</style>
