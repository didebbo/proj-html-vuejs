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
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Montserrat", sans-serif;
}
</style>
