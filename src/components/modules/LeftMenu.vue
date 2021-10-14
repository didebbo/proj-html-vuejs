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
  background-color: $edu-color-yellow;
  z-index: 5;
  top: 200px;
  padding: 0.5em;
  border-radius: 0 0.5em 0.5em 0;
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