<template>
  <div class="content">
    <div class="top-icon">
      <img src="images/Books-icon.png" alt="Books-icon" />
    </div>
    <div class="title">
      <h2>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quisquam eaque
        suscipit.
      </h2>
    </div>
    <div class="description">
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
        molestiae itaque deserunt rem velit magni, animi inventore ad rerum,
        repellat perferendis. Earum hic nam saepe nulla, fuga officia iste
        laborum.
      </p>
    </div>
    <div class="btn">
      <a href="#"> Lorem Ipsum </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "TwContent",
};
</script>

<style scoped lang="scss">
@import "../../scss/mixin";
.content {
  .top-icon {
    img {
      height: 2em;
    }
  }
  .btn {
    a {
      @include btn-yellow;
    }
  }
}
</style>