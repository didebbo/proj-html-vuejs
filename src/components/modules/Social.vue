<template>
  <div class="social">
    <div class="logo">
      <img src="/images/theme_eduprime_logo.png" alt="EduPrime Logo" />
    </div>
    <div class="description">
      Lorem ipsum, dolor sit amet consectetur adipisicing elit. Lorem ipsum,
      dolor sit amet consectetur adipisicing elit.
    </div>
    <div class="social-icons">
      <div class="row">
        <div v-for="(social, index) in socials" :key="index" class="col">
          <a :href="social.href">
            <div class="icon">
              <i :class="`${social.fa_prefix} ${social.fa_suffix}`"></i>
            </div>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Social",
  props: ["socials"],
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.social {
  .logo {
    img {
      height: 2.5em;
    }
  }
  .description {
    font-size: 0.8em;
    padding: 1.5em 0;
  }
  .social-icons {
    .row {
      display: flex;
      flex-wrap: wrap;
      .col {
        padding: 0.3em;
        a {
          color: $edu-color-white;
          text-decoration: none;

          .icon {
            position: relative;
            border: 0.1em solid $edu-color-yellow;
            border-radius: 50%;
            width: 2.5em;
            height: 2.5em;
            transition: 0.2s;
            &:hover {
              background-color: $edu-color-yellow;
              color: $edu-color-red;
              transform: rotate(360deg);
            }

            i {
              position: absolute;
              top: 50%;
              left: 50%;
              transform: translate(-50%, -50%);
            }
          }
        }
      }
    }
  }
}
</style>