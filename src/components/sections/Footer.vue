<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col social">
          <Social :socials="socials" />
        </div>
        <div class="col menu">
          <VerticalMenu :menu="menu_getEduPrime" />
        </div>
        <div class="col menu">
          <VerticalMenu :menu="menu_networking" />
        </div>
        <div class="col category">
          <SearchCategory :categories="categories" />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Social from "../modules/Social.vue";
import VerticalMenu from "../modules/VerticalMenu.vue";
import SearchCategory from "../modules/SearchCategory.vue";

export default {
  name: "Footer",
  components: {
    Social,
    VerticalMenu,
    SearchCategory,
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
      menu_getEduPrime: {
        title: "Get EduPrime",
        links: [
          {
            label: "Request a website",
            href: "#",
          },
          {
            label: "Browse Themes",
            href: "#",
          },
          {
            label: "Payment options",
            href: "#",
          },
          {
            label: "Support System",
            href: "#",
          },
          {
            label: "Checkout",
            href: "#",
          },
          {
            label: "Purchase Theme",
            href: "#",
          },
        ],
      },
      menu_networking: {
        title: "Networking",
        links: [
          {
            label: "Purchase Theme",
            href: "#",
          },
          {
            label: "Our Benefits",
            href: "#",
          },
          {
            label: "Our Theam",
            href: "#",
          },
          {
            label: "Our Services",
            href: "#",
          },
          {
            label: "Other Products",
            href: "#",
          },
          {
            label: "My Account",
            href: "#",
          },
        ],
      },
      categories: [
        {
          label: "Economy",
          href: "#",
        },
        {
          label: "Design",
          href: "#",
        },
        {
          label: "Coaching",
          href: "#",
        },
        {
          label: "Business",
          href: "#",
        },
        {
          label: "Medicine",
          href: "#",
        },
        {
          label: "Law",
          href: "#",
        },
        {
          label: "Fitnes",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";
@import "../../scss/breakpoints";

footer {
  padding: 3em 0;
  background-color: $edu-color-red;
  color: $edu-color-white;
  .container {
    > .row {
      display: flex;
      // flex-wrap: wrap;
      justify-content: center;
      // border: 0.1em solid red;
      > .col {
        display: flex;
        justify-content: center;
        // border: 0.1em solid red;
        &.social {
          width: 30%;
        }
        &.menu {
          width: 20%;
          padding: 0 1.5em;
        }
        &.category {
          width: 30%;
        }
      }
    }
  }
}
</style>
