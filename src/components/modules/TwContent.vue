<template>
  <div class="content">
    <div v-if="content.topIcon" class="top-icon">
      <img :src="`images/${content.topIcon}`" :alt="content.topIcon" />
    </div>
    <div class="title">
      <h2>
        {{ content.title }}
      </h2>
    </div>
    <div class="description">
      <p>
        {{ content.description }}
      </p>
    </div>
    <div class="btn">
      <a :href="content.btn.href">
        {{ content.btn.label }}
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "TwContent",
  props: ["content"],
};
</script>

<style scoped lang="scss">
@import "../../scss/mixin";
.content {
  .top-icon {
    padding: 0.5em 0;
    img {
      height: 2em;
    }
  }
  .description {
    font-size: 0.8em;
    padding: 2em 0;
  }
  .btn {
    a {
      @include btn-yellow;
    }
  }
}
</style>