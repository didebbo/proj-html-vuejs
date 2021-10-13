<template>
  <div class="univerityYear">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="topIcon">
            <img src="images/Clock-and-Bell.png" alt="Clock-and-Bell" />
          </div>
        </div>
        <div class="col">
          <div class="title">
            <h2>University Year</h2>
          </div>
        </div>
        <div class="col">
          <div class="timeline">
            <img src="images/Timeline-Item.png" alt="Timeline-Item" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "UniverityYear",
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.univerityYear {
  color: $edu-color-white;
  .container {
    .row {
      display: flex;
      flex-direction: column;
      align-items: center;
      .col {
        padding: 1em 0;
        .topIcon {
          height: 2.5em;
          img {
            width: 100%;
            height: 100%;
            object-fit: contain;
          }
        }
        .title {
          background-color: $edu-color-brown;
        }
      }
    }
  }
}
</style>