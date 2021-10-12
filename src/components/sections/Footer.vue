<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col">
          <Social :socials="socials" />
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
  data() {
    return {
      socials: [
        {
          fa_prefix: "fab",
          fa_suffix: "fa-facebook-f",
          href: "#",
        },
        {
          fa_prefix: "fab",
          fa_suffix: "fa-twitter",
          href: "#",
        },
        {
          fa_prefix: "fab",
          fa_suffix: "fa-instagram",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

footer {
  padding: 5em 0;
  background-color: $edu-color-red;
  color: $edu-color-white;
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
