<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col">
          <Social />
        </div>
        <div class="col">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Suscipit
          itaque nam, assumenda tenetur beatae ea ad quam natus voluptatum
          consequuntur blanditiis quas enim omnis ex maiores officiis sapiente
          reprehenderit tempore.
        </div>
        <div class="col">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Suscipit
          itaque nam, assumenda tenetur beatae ea ad quam natus voluptatum
          consequuntur blanditiis quas enim omnis ex maiores officiis sapiente
          reprehenderit tempore.
        </div>
        <div class="col">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Suscipit
          itaque nam, assumenda tenetur beatae ea ad quam natus voluptatum
          consequuntur blanditiis quas enim omnis ex maiores officiis sapiente
          reprehenderit tempore.
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Social from "../modules/Social.vue";

export default {
  name: "Footer",
  components: {
    Social,
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

footer {
  padding: 5em;
  background-color: $edu-color-red;
  .container {
    .row {
      display: flex;
      flex-wrap: wrap;
      > .col {
        width: (100% / 4);
        padding: 0 1em;
      }
    }
  }
}
</style>
