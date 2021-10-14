<template>
  <div class="leftMenu">
    <ul class="row">
      <li class="col">
        <div class="cart">
          <a href="#">
            <i class="fas fa-shopping-cart"></i>
          </a>
        </div>
      </li>
      <li class="col">
        <div class="book">
          <a href="#">
            <i class="fas fa-book-open"></i>
          </a>
        </div>
      </li>
      <li class="col">
        <div class="support">
          <a href="#">
            <i class="fas fa-life-ring"></i>
          </a>
        </div>
      </li>
    </ul>
    <div class="toggle">
      <i class="fas fa-circle"></i>
    </div>
  </div>
</template>

<script>
export default {
  name: "LeftMenu",
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.leftMenu {
  position: fixed;
  display: flex;
  align-items: center;
  background-color: $edu-color-yellow;
  z-index: 5;
  top: 200px;
  padding: 0.5em 1em 0.5em 0.5em;
  border-radius: 0 0.5em 0.5em 0;
  color: $edu-color-white;
  left: -2em;
  transition: 0.4s;

  &:hover {
    left: 0;
  }

  .toggle {
    position: absolute;
    right: -0.5em;
    padding-left: 0.5em;
    cursor: pointer;
    text-shadow: 0.2em 0 0.4em rgba(0, 0, 0, 0.4);
  }
  .row {
    display: flex;
    flex-direction: column;
    list-style: none;
    .col {
      padding: 0.2em 0;
      a {
        color: $edu-color-white;
        text-decoration: none;
      }
    }
  }
}
</style>