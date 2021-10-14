<template>
  <div id="app">
    <Header />
    <LeftMenu />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/sections/Header.vue";
import Main from "./components/sections/Main.vue";
import Footer from "./components/sections/Footer.vue";
import LeftMenu from "./components/modules/LeftMenu.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
    LeftMenu,
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
h1,
h2,
h3,
h4,
h5,
h6,
body {
  line-height: 1.2em;
}
body {
  font-family: "Montserrat", sans-serif;
  font-weight: 500;
  background-color: $edu-color-red;
  color: $edu-text-color;
  cursor: default;
}
</style>
