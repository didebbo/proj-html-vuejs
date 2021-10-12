<template>
  <div class="verticalMenu">
    <div class="title">
      <h4>
        {{ menu.title }}
      </h4>
    </div>
    <ul class="menu">
      <li v-for="(link, index) in menu.links" :key="index" class="link">
        <a :href="link.href">
          {{ link.label }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "VerticalMenu",
  props: ["menu"],
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.verticalMenu {
  display: flex;
  flex-direction: column;
  .menu {
    display: flex;
    flex-direction: column;
    list-style: none;
    padding: 1em 0;
    .link {
      font-size: 0.8em;
      padding: 0.5em 0;
      a {
        color: $edu-color-white;
        text-decoration: none;
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
}
</style>