<template>
  <div class="searchCategory">
    <div class="searchBar">
      <form action="#">
        <input type="text" placeholder="Search..." />
        <button type="submit">
          <i class="fas fa-search"></i>
        </button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "SearchCategory",
  props: ["categories"],
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.searchCategory {
  .searchBar {
    // margin: 0 1em;

    form {
      position: relative;
      display: flex;
      input {
        height: 4em;
        padding: 0 1em;
        border: 0;
        border-radius: 2em;
      }
      button {
        position: absolute;
        border: 0;
        border-radius: 2em;
        width: 4em;
        height: 4em;
        top: 0;
        right: 0;
        background-color: $edu-color-yellow;
        color: $edu-color-white;
      }
    }
  }
}
</style>