<template>
  <main>
    <section class="courses">
      <TwoColumns :data="coursesSection" />
    </section>
  </main>
</template>

<script>
import TwoColumns from "../modules/TwoColumns.vue";

export default {
  name: "Main",
  components: {
    TwoColumns,
  },
  data() {
    return {
      coursesSection: {
        imageToRight: true,
        content: {
          topIcon: "",
          title: "Lorem ipsum dolor",
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
.courses {
  background-color: $edu-color-white;
}
</style>