<template>
  <header>
    <Navbar />
  </header>
</template>

<script>
import Navbar from "../modules/Navbar.vue";
export default {
  name: "Header",
  components: {
    Navbar,
  },
};
</script>

<style scoped lang="scss">
header {
  background-color: red;
}
</style>
