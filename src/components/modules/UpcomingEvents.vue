<template>
  <div class="upcomingEvents">
    <div class="container">
      <div class="row">
        <div class="col">
          <div class="topIcon">
            <img
              src="images/upcoming-events-calendar-icon.png"
              alt="upcoming-events-calendar-icon"
            />
          </div>
        </div>
        <div class="col">
          <div class="title">
            <h2>Upcoming Events</h2>
          </div>
        </div>
        <div class="col">
          <div class="events">
            <div class="row">
              <div v-for="(event, index) in events" :key="index" class="col">
                <Card :data="event" />
              </div>
            </div>
          </div>
        </div>
        <div class="col">
          <div class="allEvents">
            <a href="#"> View All Events</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";

export default {
  name: "UpcomingEvents",
  components: {
    Card,
  },
  data() {
    return {
      events: [
        {
          date: "28/07/2021 18:30",
          title: "Coaching Session",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sed, autem eos esse voluptatibus quis numquam praesentium.",
          href: "#",
        },
        {
          date: "28/07/2021 18:30",
          title: "Coaching Session",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sed, autem eos esse voluptatibus quis numquam praesentium.",
          href: "#",
        },
        {
          date: "28/07/2021 18:30",
          title: "Coaching Session",
          description:
            "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Sed, autem eos esse voluptatibus quis numquam praesentium.",
          href: "#",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "../../scss/mixin";

.upcomingEvents {
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
        .title {
          font-size: 1.2em;
        }
        .events {
          > .row {
            display: flex;
            // border: 0.2em solid red;
            justify-content: center;
            > .col {
              // border: 0.2em solid blue;
              padding: 0 1em;
              width: (100% / 4);
            }
          }
        }
        .allEvents {
          padding: 2em 0;
          a {
            @include btn-yellow;
          }
        }
      }
    }
  }
}
</style>