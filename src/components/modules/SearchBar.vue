<template>
  <div class="searchBar">
    <form action="#">
      <input type="text" :placeholder="data.placeholder" />
      <button type="submit" @click.prevent>
        <i :class="`${data.btnIcon.prefix} ${data.btnIcon.suffix}`"></i>
      </button>
    </form>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  props: ["data"],
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.searchBar {
  form {
    position: relative;
    display: flex;

    input {
      width: 100%;
      padding: 0 4.5em 0 1em;
      border: 0;
      border-radius: 2em;
      height: 4em;
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
      cursor: pointer;
      transition: 0.2s;
      &:hover {
        filter: brightness(1.1);
      }
    }
  }
}
</style>