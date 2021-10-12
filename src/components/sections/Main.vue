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
          topIcon: "Books-icon.png",
          title: `Thousands of courses for any type of student`,
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
        molestiae itaque deserunt rem velit magni, animi inventore ad rerum,
        repellat perferendis. Earum hic nam saepe nulla, fuga officia iste
        laborum.`,
          btn: {
            label: `Browse all courses`,
            href: `#`,
          },
        },
        banner: "Graduation-Illustration.png",
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