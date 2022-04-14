<template>
  <div class="home">
    <!-- Nav Section -->
    <NavBar></NavBar>
    <!-- Call to Action Section -->
    <CallToAction></CallToAction>
    <!-- Courses Section -->
    <div></div>
    <!-- Events Section -->
    <div></div>
    <!-- Membership Section -->
    <div></div>
    <!-- Numbers Section -->
    <div></div>
    <!-- Form Section -->
    <div></div>
    <!-- Footer Section -->
    <div></div>

  </div>
</template>

<script>
import NavBar from '@/components/NavBar/NavBar.vue'
import CallToAction from '@/components/CallToAction/CallToAction.vue'
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    NavBar,
    CallToAction,
  }
}
</script>
