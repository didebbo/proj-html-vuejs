<template>
  <main>
    <section class="courses">
      <TwoColumns :data="coursesSection" />
    </section>
    <section class="faculties">
      <Faculties />
    </section>
    <section class="univerisyYear">
      <UniverityYear />
    </section>
    <section class="subscribe">
      <Subscribe />
    </section>
  </main>
</template>

<script>
import TwoColumns from "../modules/TwoColumns.vue";
import Faculties from "../modules/Faculties.vue";
import Subscribe from "../modules/Subscribe.vue";
import UniverityYear from "../modules/UniverityYear.vue";

export default {
  name: "Main",
  components: {
    TwoColumns,
    Faculties,
    Subscribe,
    UniverityYear,
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

section {
  padding: 2em 0;
}
.courses,
.faculties {
  background-color: $edu-color-white;
}
</style>