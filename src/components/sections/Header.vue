<template>
  <header>
    <Navbar :menu="menu" />
  </header>
</template>

<script>
import Navbar from "../modules/Navbar.vue";
export default {
  name: "Header",
  components: {
    Navbar,
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
  background-color: $edu-color-red;
}
</style>
