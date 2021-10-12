<template>
  <div class="banner">
    <img :src="`images/${banner}`" :alt="`images/${banner}`" />
  </div>
</template>

<script>
export default {
  name: "TwBanner",
  props: ["banner"],
};
</script>

<style scoped lang="scss">
.banner {
  img {
    max-width: 100%;
    height: 15em;
    object-fit: contain;
  }
}
</style>