<template>
  <div class="latestCourses">
    <div class="container">
      <div class="title">
        <h2>Latest Courses</h2>
      </div>
      <div class="courses">
        <div class="row">
          <div v-for="(course, index) in data" :key="index" class="col">
            <CardCourses :data="course" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardCourses from "./CardCourses.vue";
export default {
  name: "LatestCourses",
  props: ["data"],
  components: {
    CardCourses,
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/breakpoints";
.latestCourses {
  .container {
    max-width: $lg;
    .courses {
      //   border: 0.2em solid red;
      padding: 1em 0;
      .row {
        position: relative;
        left: -1em;
        display: flex;
        // align-items: flex-start;
        flex-wrap: wrap;
        .col {
          //   border: 0.2em solid red;
          padding: 1em;
          width: (100% / 4);
          > * {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
}
</style>