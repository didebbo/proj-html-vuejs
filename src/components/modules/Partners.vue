<template>
  <div class="partners">
    <div class="container">
      <div class="title">
        <h2>Partners</h2>
      </div>
      <div class="description">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit
          maiores est, consequuntur aperiam, earum provident.
        </p>
      </div>
      <div class="partners-brand">
        <div class="row">
          <div v-for="(partner, index) in data" :key="index" class="col">
            <div class="brand">
              <a :href="partner.href">
                <img :src="`images/${partner.src}`" :alt="partner.src" />
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Partners",
  props: ["data"],
};
</script>

<style scoped lang="scss">
.partners {
  text-align: center;
  .container {
    .description {
      width: 50%;
      margin: auto;
      padding: 2em 0;
      font-size: 0.8em;
    }
    .partners-brand {
      padding: 2em 0 5em 0;
      > .row {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        > .col {
          padding: 1em;
          height: 5em;
          //   border: 0.2em solid red;
          .brand {
            // border: 0.2em solid blue;
            width: 100%;
            height: 100%;
            a {
              opacity: 0.4;
              &:hover {
                opacity: 0.8;
              }
              img {
                width: 100%;
                height: 100%;
                object-fit: contain;
              }
            }
          }
        }
      }
    }
  }
}
</style>