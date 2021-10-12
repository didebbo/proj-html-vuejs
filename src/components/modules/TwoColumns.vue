<template>
  <div class="two-columns">
    <div class="container">
      <div class="row">
        <div class="col">
          <TwContent v-if="data.imageToRight" :content="data.content" />
          <TwBanner v-else :banner="data.banner" />
        </div>
        <div class="col">
          <TwContent v-if="!data.imageToRight" :content="data.content" />
          <TwBanner v-else :banner="data.banner" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TwContent from "./TwContent.vue";
import TwBanner from "./TwBanner.vue";

export default {
  name: "TwoColumns",
  props: ["data"],
  components: {
    TwContent,
    TwBanner,
  },
};
</script>

<style scoped lang="scss">
.two-columns {
  .container {
    .row {
      //   border: 0.2em solid green;
      display: flex;
      justify-content: center;
      padding: 2em 0;
      > .col {
        max-width: (100% / 2);
        // border: 0.2em solid red;
        padding: 0 2em;
      }
    }
  }
}
</style>