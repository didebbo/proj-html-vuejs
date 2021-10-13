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
            <div class="row">
              <div class="col">
                <div class="row right">
                  <div class="col">
                    <div class="demoClasses">
                      <div class="title">
                        <h5>Demo Classes</h5>
                      </div>
                      <div class="description">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Aspernatur quam dolorum autem delectus incidunt qui
                        nihil ullam quae dolor reprehenderit.
                      </div>
                    </div>
                  </div>
                  <div class="col">
                    <div class="graduationDay">
                      <div class="title">
                        <h5>Graduation Day</h5>
                      </div>
                      <div class="description">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Aspernatur quam dolorum autem delectus incidunt qui
                        nihil ullam quae dolor reprehenderit.
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col">
                <img src="images/Timeline-Item.png" alt="Timeline-Item" />
              </div>
              <div class="col">
                <div class="row left">
                  <div class="col">
                    <div class="orientation">
                      <div class="title">
                        <h5>Orientation</h5>
                      </div>
                      <div class="description">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Aspernatur quam dolorum autem delectus incidunt qui
                        nihil ullam quae dolor reprehenderit.
                      </div>
                    </div>
                  </div>
                  <div class="col">
                    <div class="Evolution">
                      <div class="title">
                        <h5>Evolution</h5>
                      </div>
                      <div class="description">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit.
                        Aspernatur quam dolorum autem delectus incidunt qui
                        nihil ullam quae dolor reprehenderit.
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
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
    > .row {
      display: flex;
      flex-direction: column;
      align-items: center;
      > .col {
        padding: 1em 0;
        .topIcon {
          height: 2.5em;
          img {
            width: 100%;
            height: 100%;
            object-fit: contain;
          }
        }
        > .title {
          background-color: $edu-color-brown;
        }
        .timeline {
          > .row {
            display: flex;
            flex-direction: column;
            > .col {
              > .row {
                // border: 0.2em solid blue;
                padding: 1em 0;
                display: flex;
                &.right {
                  justify-content: flex-end;
                  .col:last-child {
                    margin-right: 6em;
                  }
                  .col:first-child {
                    margin-right: 3em;
                  }
                }
                &.left {
                  .col:first-child {
                    margin-left: 1em;
                  }
                  .col:last-child {
                    margin-left: 4em;
                  }
                }
                > .col {
                  //   border: 0.2em solid red;
                  width: (100% / 3);
                  text-align: center;
                  .description {
                    font-size: 0.8em;
                    opacity: 0.8;
                    padding-top: 1em;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
}
</style>