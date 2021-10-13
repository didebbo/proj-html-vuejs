<template>
  <header>
    <div class="cover"></div>
    <div class="on-cover">
      <Navbar :menu="menu" />
      <Hero />
      <div class="separator"></div>
    </div>
  </header>
</template>

<script>
import Navbar from "../modules/Navbar.vue";
import Hero from "../modules/Hero.vue";
export default {
  name: "Header",
  components: {
    Navbar,
    Hero,
  },
  data() {
    return {
      menu: [
        {
          label: "Home",
          active: true,
          dropdown: true,
          src: "#",
        },
        {
          label: "Courses",
          active: false,
          dropdown: true,
          src: "#",
        },
        {
          label: "About Us",
          active: false,
          dropdown: false,
          src: "#",
        },
        {
          label: "News",
          active: false,
          dropdown: true,
          src: "#",
        },
        {
          label: "Pages",
          active: false,
          dropdown: true,
          src: "#",
        },
        {
          label: "Contact",
          active: false,
          dropdown: false,
          src: "#",
        },
        {
          label: "Purchase",
          active: false,
          dropdown: false,
          src: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
header {
  position: relative;
  background-color: $edu-color-red;
  background-image: url("/images/theme_slider2_bg-1.jpg");
  background-size: cover;
  background-position: top;
  .cover {
    position: absolute;
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: $edu-color-red;
    opacity: 0.9;
    z-index: 1;
  }
  .on-cover {
    position: relative;
    display: block;
    z-index: 2;
    overflow: hidden;
    .separator {
      position: relative;
      bottom: -5px;
      display: flex;
      width: 100vw;
      height: 128px;
      background-image: url("/images/Wave-1.png");
      background-size: contain;
      background-repeat: repeat-x;
      background-position: bottom;
    }
  }
}
</style>
