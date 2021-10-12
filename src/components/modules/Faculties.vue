<template>
  <div class="faculties">
    <div class="container">
      <div class="title">
        <h2>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed itaque
          labore nihil perferendis aliquid temporibus asperiores.
        </h2>
      </div>
      <div class="description">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Soluta animi,
        provident omnis repellendus eum aliquid, excepturi quibusdam suscipit
        dolorum ea dolorem? Eius nesciunt fuga eaque debitis aperiam dolorum vel
        doloribus.
      </div>
      <div class="menu-cards">
        <ul class="row">
          <li class="col">
            <div class="card">
              <div class="image">
                <img src="images/Gavel-v2.png" alt="Gavel-v2" />
              </div>
              <div class="title">
                <h5>Lorem Ipsum</h5>
              </div>
            </div>
          </li>
          <li class="col">
            <div class="card active">
              <div class="image">
                <img src="images/Gavel-v2.png" alt="Gavel-v2" />
              </div>
              <div class="title">
                <h5>Lorem Ipsum</h5>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Faculties",
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.faculties {
  .container {
    .menu-cards {
      .row {
        //   border: 0.2em solid red;
        display: flex;
        list-style: none;
        .col {
          // border: 0.2em solid green;
          .card {
            //   border: 0.2em solid blue;
            padding: 1em;
            &.active {
              background-color: $edu-color-red;
              img {
                filter: brightness(200%);
              }
              .title {
                color: $edu-color-white;
              }
            }
            .image {
              img {
                width: 5em;
                height: 5em;
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