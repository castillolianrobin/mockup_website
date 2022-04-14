<template>
  <div class="bg-blue-800 p-10 py-20">
    <div class="text-white text-center">
      <h2 class="text-2xl font-semibold">Events</h2>
      <h5 class="mt-1 font-light">
        Join Upcoming CPD Accredited Training, Events and Seminars
      </h5>
    </div>
    <div class="mt-12 grid md:grid-cols-2 gap-5">
      <EventCard
        v-for="(event, index) in events"
        :key="`event-${index}`"
        :img="event.img"
        :title="event.title"
        :date="event.date"
        :description="event.description"
      ></EventCard>
    </div>

    <AppButton outline color="white" class="block mx-auto mt-10">
      View all events
    </AppButton>
  </div>
</template>

<script>
import AppButton from "../app/AppButton.vue";
import EventCard from "./EventCard.vue";
export default {
  components: { EventCard, AppButton },
  data() {
    return {
      events: [
        {
          img: require("@/assets/events/event-1.jpg"),
          title: "Lorem Ipsum Set Dolor",
          date: "Jan 27, 2022",
          description:
            "Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil iure reprehenderit qui in ea voluptate velit esse quam nihil...",
        },
        {
          img: require("@/assets/events/event-2.jpg"),
          title: "Lorem Ipsum Set Dolor",
          date: "Jan 27, 2022",
          description:
            "Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil iure reprehenderit qui in ea voluptate velit esse quam nihil...",
        },
        {
          img: require("@/assets/events/event-3.jpg"),
          title: "Lorem Ipsum Set Dolor",
          date: "Jan 27, 2022",
          description:
            "Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil iure reprehenderit qui in ea voluptate velit esse quam nihil...",
        },
        {
          img: require("@/assets/events/event-4.jpg"),
          title: "Lorem Ipsum Set Dolor",
          date: "Jan 27, 2022",
          description:
            "Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil iure reprehenderit qui in ea voluptate velit esse quam nihil...",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
