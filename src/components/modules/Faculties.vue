<template>
  <div class="faculties">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="title">
            <h2>Faculties avaiable at EduPrime</h2>
          </div>
        </div>
        <div class="col">
          <div class="description">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo
            accusantium rerum nisi omnis deserunt! Sint inventore veniam qui sit
            minima consequatur vero, modi dolore laborum at obcaecati in atque
            ad.
          </div>
        </div>
        <div class="col">
          <div class="menu-cards">
            <ul class="row">
              <li class="col">
                <div class="card"></div>
              </li>
              <li
                v-for="(menuFacultie, index) in menuFaculties"
                :key="index"
                class="col"
                @click="setThisFacultie(index)"
              >
                <div class="card" :class="isCurrentFacultie(index)">
                  <div class="content">
                    <div class="image">
                      <img
                        :src="`images/${menuFacultie.src}`"
                        alt="menuFacultie.src"
                      />
                    </div>
                    <div class="title">
                      <h6>{{ menuFacultie.title }}</h6>
                    </div>
                  </div>
                </div>
              </li>
              <li class="col">
                <div class="card"></div>
              </li>
            </ul>
          </div>
        </div>
        <div class="col">
          <TwoColumns :data="currentFacultieSection" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TwoColumns from "./TwoColumns.vue";
export default {
  name: "Faculties",
  components: {
    TwoColumns,
  },
  data() {
    return {
      currentFacultie: 0,
      menuFaculties: [
        {
          src: "Gavel-v2.png",
          title: "Low Faculty",
          facultieSection: {
            content: {
              title: "Low Faculty",
              btn: {
                href: `#`,
              },
            },
            banner: "Gavel-Illustration-e1556884768193.png",
          },
        },
        {
          src: "Coins-tabs-v2.png",
          title: "Economy",
          facultieSection: {
            content: {
              title: "Economy",
              btn: {
                href: `#`,
              },
            },
            banner: "Economy.png",
          },
        },
        {
          src: "Medicine-tabs-v2.png",
          title: "Medicine",
          facultieSection: {
            content: {
              title: "Medicine",
              btn: {
                href: `#`,
              },
            },
            banner: "Medicine.png",
          },
        },
        {
          src: "Computer-tabs-v2.png",
          title: "Computer Science",
          facultieSection: {
            content: {
              title: "Computer Science",
              btn: {
                href: `#`,
              },
            },
            banner: "Computer-Science.png",
          },
        },
        {
          src: "Palette-tabs-v2.png",
          title: "Graphic Design",
          facultieSection: {
            content: {
              title: "Graphic Design",
              btn: {
                href: `#`,
              },
            },
            banner: "Graphic-Design.png",
          },
        },
      ],
      currentFacultieSection: {
        imageToRight: false,
        content: {
          title: "",
          description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Nostrum
        molestiae itaque deserunt rem velit magni, animi inventore ad rerum,
        repellat perferendis. Earum hic nam saepe nulla, fuga officia iste
        laborum.`,
          btn: {
            label: `Read More`,
            href: `#`,
            bgColor: "#e56768",
          },
        },
        banner: "",
      },
    };
  },
  methods: {
    setThisFacultie(index) {
      this.currentFacultie = index;
    },
    isCurrentFacultie(index) {
      if (index == this.currentFacultie) {
        this.currentFacultieSection.content.title =
          this.menuFaculties[index].facultieSection.content.title;
        this.currentFacultieSection.banner =
          this.menuFaculties[index].facultieSection.banner;
        return "active";
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.faculties {
  .container {
    > .row {
      display: flex;
      flex-direction: column;
      // align-items: center;
      // border: 0.2em solid red;

      > .col {
        // border: 0.2em solid green;
        padding: 2em 0;
        display: flex;
        justify-content: center;
        .description {
          text-align: center;
          font-size: 0.8em;
          max-width: 50%;
        }
        .menu-cards {
          // border: 0.2em solid blue;
          width: 100%;
          ul {
            // border: 0.2em solid red;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            list-style: none;
            li {
              // border: 0.2em solid green;
              cursor: pointer;
              width: (100% / 7);
              .card {
                position: relative;
                // border: 0.2em solid orange;
                box-shadow: 0 0.1em 0.1em lightgray;
                width: 100%;
                &::after {
                  display: block;
                  content: "";
                  padding-top: 100%;
                  // width: 0.1em;
                  // background-color: red;
                }
                &.active {
                  background-color: $edu-color-red;
                  box-shadow: none;
                  img {
                    filter: brightness(200%);
                  }
                  .content {
                    .title {
                      color: $edu-color-white;
                    }
                  }
                }
                .content {
                  position: absolute;
                  // border: 0.2em solid yellow;
                  top: 0;
                  left: 0;
                  width: 100%;
                  height: 100%;
                  display: flex;
                  flex-direction: column;
                  align-items: center;
                  justify-content: center;
                  .image {
                    width: 50%;
                    height: 50%;
                    img {
                      width: 100%;
                      height: 100%;
                      object-fit: contain;
                    }
                  }
                  .title {
                    margin-top: 0.5em;
                    color: $edu-color-red;
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