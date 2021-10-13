<template>
  <div class="card">
    <div class="row">
      <div class="col">
        <div class="title">
          <h4>
            {{ data.title }}
          </h4>
        </div>
      </div>
      <div class="col">
        <div class="date">
          <i class="far fa-calendar-alt"></i>
          <small>
            {{ data.date }}
          </small>
        </div>
      </div>
      <div class="col">
        <div class="description">
          {{ data.description }}
        </div>
      </div>
      <div class="btn">
        <a :href="data.href">
          <i class="fas fa-plus"></i>
          <span> Find More </span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["data"],
};
</script>

<style scoped lang="scss">
// @import "../../scss/colors";
@import "../../scss/mixin";
.card {
  position: relative;
  background-color: $edu-color-white;
  color: $edu-text-color;
  padding: 2em;
  border-radius: 0.5em;
  .row {
    display: flex;
    flex-direction: column;
    align-items: center;
    .col {
      padding: 0.2em 0;
      .date,
      .description {
        opacity: 0.6;
      }
      .date {
        font-size: 0.8em;
        > * {
          padding: 0 0.1em;
        }
      }
      .description {
        font-size: 0.6em;
        line-height: 1.5em;
      }
    }
    .btn {
      position: absolute;
      bottom: 0;
      left: 50%;
      transform: translate(-50%, 50%);
      font-size: 0.6em;
      a {
        @include btn-yellow($edu-color-red);
        box-shadow: 0 0.2em 0.2em rgba(0, 0, 0, 0.1);
      }
    }
  }
}
</style>