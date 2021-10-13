<template>
  <main>
    <section class="courses">
      <TwoColumns :data="courses" />
    </section>
    <section class="faculties">
      <Faculties />
      <div class="separator"></div>
    </section>
    <section class="univerisyYear">
      <UniverityYear />
    </section>
    <section class="upcomingEvents">
      <UpcomingEvents />
    </section>
    <section class="methods">
      <div class="separator"></div>
      <TwoColumns :data="methods" />
    </section>
    <section class="fees">
      <TwoColumns :data="fees" />
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
import UpcomingEvents from "../modules/UpcomingEvents.vue";

export default {
  name: "Main",
  components: {
    TwoColumns,
    Faculties,
    Subscribe,
    UniverityYear,
    UpcomingEvents,
  },
  data() {
    return {
      courses: {
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
      methods: {
        imageToRight: true,
        content: {
          topIcon: "Exam-icon.png",
          title: `The most efficient examination method`,
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
        molestiae itaque deserunt rem velit magni, animi inventore ad rerum,
        repellat perferendis. Earum hic nam saepe nulla, fuga officia iste
        laborum.`,
          btn: {
            label: `Discover the Method`,
            href: `#`,
            bgColor: "#e56768",
          },
        },
        banner: "Exam-Illustration.png",
      },
      fees: {
        imageToRight: false,
        content: {
          topIcon: "Exam-icon-1.png",
          title: `Variable fees for international students`,
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
        molestiae itaque deserunt rem velit magni, animi inventore ad rerum,
        repellat perferendis. Earum hic nam saepe nulla, fuga officia iste
        laborum.`,
          btn: {
            label: `List of Fees`,
            href: `#`,
            bgColor: "#e56768",
          },
        },
        banner: "Exam-Illustration.png",
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
.faculties,
.methods,
.fees {
  background-color: $edu-color-white;
}

main {
  .courses {
    background-image: url("/images/home-background.png");
    background-size: cover;
    background-position: top right;
  }
  .faculties {
    position: relative;
    padding-bottom: 0;
    overflow: hidden;
    .separator {
      position: relative;
      position: relative;
      bottom: -5px;
      display: flex;
      width: 100vw;
      height: 128px;
      background-image: url("/images/svg-0.svg");
      background-size: contain;
      background-repeat: repeat-x;
      background-position: bottom;
    }
  }
  .methods {
    position: relative;
    padding-top: 0;
    overflow: hidden;
    .separator {
      position: relative;
      top: -5px;
      display: flex;
      width: 100vw;
      height: 128px;
      background-image: url("/images/svg-1.svg");
      background-size: contain;
      background-repeat: repeat-x;
      background-position: top;
    }
  }
}
</style>