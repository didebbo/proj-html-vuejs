<template>
  <section class="hero">
    <div class="container">
      <div class="title">
        <h1>Key to your success</h1>
      </div>
      <div class="description">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae corporis
        earum rem labore sit dolorem quidem hic vel nesciunt.
      </div>
      <div class="actions">
        <a href="#" class="btn-courses"> Search Courses </a>
        <a href="#" class="btn-university"> Apply for univerisy </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
@import "../../scss/mixin";

.hero {
  padding: 4em 0;
  color: $edu-color-white;
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
    .title {
      font-size: 1.2em;
    }
    .description {
      padding: 2em 0;
      width: 50%;
      font-size: 0.8em;
      font-weight: 500;
      text-align: center;
      line-height: 2em;
    }
    .actions {
      a {
        @include btn-yellow;
        margin: 0 1em;
      }
      .btn-university {
        @include btn-yellow($edu-color-white, $edu-color-red);
      }
    }
  }
}
</style>