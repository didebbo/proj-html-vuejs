<template>
  <div class="searchCategory">
    <SearchBar :data="searchBar" />
    <div class="categories">
      <div class="title">
        <h4>Search Categories</h4>
      </div>
      <ul class="row">
        <li v-for="(categorie, index) in categories" :key="index" class="col">
          <div class="categorie">
            <a :href="categorie.href">
              {{ categorie.label }}
            </a>
          </div>
        </li>
      </ul>
    </div>
    <div class="copyright">
      <span>ModelTheme. All Right Reserved.</span>
    </div>
  </div>
</template>

<script>
import SearchBar from "./SearchBar.vue";
export default {
  name: "SearchCategory",
  props: ["categories"],
  components: {
    SearchBar,
  },
  data() {
    return {
      searchBar: {
        placeholder: "Search...",
        btnIcon: {
          prefix: "fas",
          suffix: "fa-search",
        },
      },
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.searchCategory {
  display: flex;
  flex-direction: column;
  .categories {
    // border: 0.1em solid red;
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    padding: 2em 0;
    .row {
      //   border: 0.1em solid blue;
      display: flex;
      flex-wrap: wrap;
      list-style: none;
      justify-content: flex-end;
      padding: 1em 0;
      .col {
        padding: 0.2em;
        .categorie {
          border: 0.1em solid $edu-color-white;
          border-radius: 2em;
          font-size: 0.6em;
          text-transform: uppercase;
          a {
            display: inline-block;
            padding: 0.6em 1.2em;
            color: $edu-color-white;
            text-decoration: none;
          }
          &:hover {
            background-color: $edu-color-white;
            a {
              color: $edu-text-color;
            }
          }
        }
      }
    }
  }
  .copyright {
    align-self: flex-end;
    color: $edu-color-yellow;
    font-size: 0.8em;
    // font-weight: 600;
  }
}
</style>