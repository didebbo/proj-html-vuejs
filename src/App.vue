<template>
  <div id="app">
    <Header />

    <main>
      <!-- TODO Main Elements -->
      This is the Main!
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./components/sections/Header.vue";
import Footer from "./components/sections/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
};
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
</style>
