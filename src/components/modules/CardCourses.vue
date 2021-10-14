<template>
  <div class="cardCourses">
    <div class="topIcon">
      <img :src="`images/${data.topIcon}`" :alt="data.src" />
    </div>
    <div class="title">
      <h5>
        {{ data.title }}
      </h5>
    </div>
    <div class="teacher">
      <i class="far fa-user"></i>
      <span> Teacher: </span>
      <span style="font-weight: bold">
        {{ data.teacher }}
      </span>
    </div>
    <div class="price">
      <i class="fas fa-money-bill"></i>
      <span> Price: </span>
      <span style="font-weight: bold">
        {{ data.price }}
      </span>
    </div>
    <div class="btn">
      <a :href="data.href">
        <i class="far fa-eye"></i>
        <span> View Course </span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardCourses",
  props: ["data"],
};
</script>

<style scoped lang="scss">
@import "../../scss/mixin";

.cardCourses {
  position: relative;
  background-color: $edu-color-white;
  box-shadow: 0 0 0.5em lightgray;
  padding: 2em 1em;
  text-align: center;
  border-radius: 0.2em;

  > * {
    padding: 0.2em 0;
  }

  .title {
    padding-top: 1em;
  }

  .topIcon {
    height: 4em;
    img {
      width: 100%;
      height: 100%;
      object-fit: contain;
    }
  }
  .teacher,
  .price {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 0.6em;
    > * {
      padding: 0 0.2em;
    }
  }
  .btn {
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translate(-50%, 50%);
    a {
      @include btn-yellow($edu-color-red);
      display: flex;
      align-items: center;
      font-size: 0.6em;
      > * {
        padding: 0 0.2em;
      }
    }
  }
}
</style>