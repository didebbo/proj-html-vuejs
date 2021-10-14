<template>
  <div class="faculties">
    <div class="row">
      <div class="col">
        <div class="container">
          <div class="title">
            <h2>Faculties avaiable at EduPrime</h2>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="container">
          <div class="description">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Explicabo
            accusantium rerum nisi omnis deserunt! Sint inventore veniam qui sit
            minima consequatur vero, modi dolore laborum at obcaecati in atque
            ad.
          </div>
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
        <div class="container">
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
      currentFacultie: 1,
      menuFaculties: [
        {
          src: "Gavel-v2.png",
          title: "Low Faculty",
          facultieSection: {
            imageToRight: false,
            content: {
              title: "Low Faculty",
              description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis blanditiis hic minus aperiam culpa at consectetur praesentium debitis aspernatur recusandae laudantium quae fugit vitae, velit voluptatum obcaecati ad placeat amet.`,
              btn: {
                label: `Read More`,
                href: `#`,
                bgColor: "#e56768",
              },
            },
            banner: "Gavel-Illustration-e1556884768193.png",
          },
        },
        {
          src: "Coins-tabs-v2.png",
          title: "Economy",
          facultieSection: {
            imageToRight: true,
            content: {
              title: "Economy",
              description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Labore consequuntur fuga suscipit! Nulla veritatis, optio pariatur atque ut similique, est vero quis totam provident, hic fugiat quibusdam odio vel aut.`,
              btn: {
                label: `Read More`,
                href: `#`,
                bgColor: "#e56768",
              },
            },
            banner: "Economy.png",
          },
        },
        {
          src: "Medicine-tabs-v2.png",
          title: "Medicine",
          facultieSection: {
            imageToRight: false,
            content: {
              title: "Medicine",
              description: `Lorem, ipsum dolor sit amet consectetur adipisicing elit. Minima eaque voluptates, aspernatur ab sint fugit dolores, natus doloribus illum voluptate earum, hic commodi. Consectetur, illum facilis sapiente voluptas accusantium expedita?`,
              btn: {
                label: `Read More`,
                href: `#`,
                bgColor: "#e56768",
              },
            },
            banner: "Medicine.png",
          },
        },
        {
          src: "Computer-tabs-v2.png",
          title: "Computer Science",
          facultieSection: {
            imageToRight: true,
            content: {
              title: "Computer Science",
              description: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptas id incidunt soluta, quibusdam, est aliquid et quis ipsa eum cupiditate ratione nam delectus dolores hic, corporis amet fugit vel voluptate.`,
              btn: {
                label: `Read More`,
                href: `#`,
                bgColor: "#e56768",
              },
            },
            banner: "Computer-Science.png",
          },
        },
        {
          src: "Palette-tabs-v2.png",
          title: "Graphic Design",
          facultieSection: {
            imageToRight: false,
            content: {
              title: "Graphic Design",
              description: `Lorem ipsum dolor sit amet consectetur adipisicing elit. Iste aut minima quas, in totam repudiandae porro praesentium nam laborum molestias, vel incidunt perferendis vitae ipsa quam dolor recusandae saepe harum?`,
              btn: {
                label: `Read More`,
                href: `#`,
                bgColor: "#e56768",
              },
            },
            banner: "Graphic-Design.png",
          },
        },
      ],
      currentFacultieSection: null,
    };
  },
  methods: {
    setThisFacultie(index) {
      this.currentFacultie = index;
    },
    isCurrentFacultie(index) {
      if (index == this.currentFacultie) {
        this.currentFacultieSection = this.menuFaculties[index].facultieSection;
        return "active";
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/colors";

.faculties {
  > .row {
    display: flex;
    flex-direction: column;
    // align-items: center;
    // border: 0.2em solid red;

    > .col {
      // border: 0.2em solid green;
      padding: 2em 0;
      // display: flex;
      // justify-content: center;
      .description {
        text-align: center;
        font-size: 0.8em;
        max-width: 50%;
      }
      .container {
        display: flex;
        justify-content: center;
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
</style>