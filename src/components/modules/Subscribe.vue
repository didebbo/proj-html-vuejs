<template>
  <div class="subscribe">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="title">
            <h2>Subscribe now to our newsletter</h2>
          </div>
        </div>
        <div class="col">
          <SearchBar :data="searchBar" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SearchBar from "./SearchBar.vue";

export default {
  name: "Subscribe",
  components: {
    SearchBar,
  },
  data() {
    return {
      searchBar: {
        btnIcon: {
          prefix: "fas",
          suffix: "fa-paper-plane",
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
.subscribe {
  .container {
    .row {
      display: flex;
      //   border: 0.2em solid red;
      align-items: center;
      .col {
        padding: 0 2em;
        // border: 0.2em solid blue;
        flex-grow: 1;
        .title {
          color: $edu-color-white;
        }
      }
    }
  }
}
</style>