<template>
  <div class="bg-blue-800 p-10 py-20">
    <div class="text-white text-center">
      <h2 class="text-2xl font-semibold">Events</h2>
      <h5 class="mt-1 font-light">Join Upcoming CPD Accredited Training, Events and Seminars</h5>
    </div>
    <div class="mt-12 grid md:grid-cols-2 gap-5">
      <EventCard v-for="event in 4" :key="event"></EventCard>
    </div>

    <AppButton outline color="white" class="block mx-auto mt-10">
      View all events
    </AppButton>
  </div>
</template>

<script>
import AppButton from '../app/AppButton.vue'
import EventCard from './EventCard.vue'
  export default {
  components: { EventCard, AppButton },
    
  }
</script>

<style lang="scss" scoped>

</style>