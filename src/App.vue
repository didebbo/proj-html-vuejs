<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/sections/Header.vue";
import Main from "./components/sections/Main.vue";
import Footer from "./components/sections/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;700&display=swap");
@import "./scss/colors";
@import "./scss/common";
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Montserrat", sans-serif;
  font-weight: 500;
  background-color: $edu-color-red-opaque;
  color: $edu-text-color;
}
</style>
