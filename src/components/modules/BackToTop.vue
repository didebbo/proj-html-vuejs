<template>
  <div class="backToTop">
    <a href="#app">
      <i class="fas fa-chevron-up"></i>
    </a>
    <div class="toggle">
      <i class="fas fa-circle"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "BackToTop",
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.backToTop {
  position: fixed;
  display: flex;
  align-items: center;
  background-color: $edu-color-yellow;
  z-index: 5;
  bottom: 20px;
  padding: 0.5em 0.5em 0.5em 1em;
  border-radius: 0.5em 0 0 0.5em;
  color: $edu-color-white;
  right: -1.8em;
  transition: 0.4s;
  &:hover {
    right: 0px;
  }
  a {
    color: $edu-color-white;
    text-decoration: none;
  }
  .toggle {
    position: absolute;
    left: -0.5em;
    padding-right: 0.5em;
    cursor: pointer;
    text-shadow: 0.2em 0 0.4em rgba(0, 0, 0, 0.4);
  }
}
</style>