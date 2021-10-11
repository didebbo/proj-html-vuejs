<template>
  <nav>
    <div class="logo">
      <img src="images/theme_eduprime_logo.png" alt="EduPrime Logo" />
    </div>
    <div class="items">
      <ul class="row">
        <li class="col">
          <div class="item">
            <a href="#">
              <h5>Item</h5>
            </a>
          </div>
        </li>
        <li class="col">
          <div class="item">
            <a href="#">
              <h5>Item</h5>
            </a>
          </div>
        </li>
        <li class="col">
          <div class="item">
            <a href="#">
              <h5>Item</h5>
            </a>
          </div>
        </li>
      </ul>
    </div>
    <div class="btn-courses">
      <button>
        <p>View courses</p>
      </button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style scoped lang="scss">
nav {
  display: flex;
  align-items: center;
  padding: 1em 1.5em;
  // justify-content: space-between;
  .logo {
    img {
      height: 2.5em;
    }
  }
  .items {
    margin-left: auto;
    .row {
      display: flex;
      list-style: none;

      .col {
        padding: 0 0.5em;
      }
    }
  }
  .btn-courses {
    margin-left: 1em;
    buttn {
    }
  }
}
</style>