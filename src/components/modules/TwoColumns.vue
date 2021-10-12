<template>
  <div class="two-columns">
    <div class="container">
      <div class="row">
        <div class="col">
          <TwContent />
        </div>
        <div class="col">
          <div class="banner">
            <img
              src="images/Graduation-Illustration.png"
              alt="Graduation-Illustration"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TwContent from "./TwContent.vue";

export default {
  name: "TwoColumns",
  props: ["data"],
  components: {
    TwContent,
  },
};
</script>

<style scoped lang="scss">
.two-columns {
  .container {
    .row {
      border: 0.2em solid green;
      display: flex;
      justify-content: center;
      > .col {
        max-width: (100% / 2);
        border: 0.2em solid red;
        padding: 0 1em;

        .banner {
          img {
            max-width: 100%;
            height: 15em;
            object-fit: contain;
          }
        }
      }
    }
  }
}
</style>