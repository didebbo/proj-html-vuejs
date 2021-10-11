<template>
  <nav>
    <div class="logo">
      <img src="images/theme_eduprime_logo.png" alt="EduPrime Logo" />
    </div>
    <div class="items">
      <ul class="row">
        <li v-for="(item, index) in menu" :key="index" class="col">
          <div class="item">
            <a :href="item.src" :class="{ active: item.active }">
              <h5>{{ item.label }}</h5>
              <i v-if="item.dropdown" class="fas fa-caret-down"></i>
            </a>
          </div>
        </li>
      </ul>
    </div>
    <div class="btn-courses">
      <a href="#"> View Courses </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  props: ["menu"],
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
@import "../../scss/mixin";
nav {
  display: flex;
  align-items: center;
  padding: 1em 1.5em;
  .logo {
    img {
      height: 2.5em;
    }
  }
  .items {
    margin-left: auto;
    .row {
      display: flex;
      list-style: none;

      .col {
        padding: 0 0.5em;
        a {
          display: flex;
          align-items: center;
          text-decoration: none;
          color: $edu-color-white;
          font-size: 1.1em;
          i {
            padding: 0 0.4em;
            font-size: 0.8em;
          }
          &.active {
            color: $edu-color-yellow;
          }
        }
      }
    }
  }
  .btn-courses {
    margin-left: 1em;
    a {
      @include btn-yellow;
      text-transform: uppercase;
      font-size: 0.9em;
    }
  }
}
</style>