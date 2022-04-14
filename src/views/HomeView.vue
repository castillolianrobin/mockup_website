<template>
  <div class="home">
    <!-- Nav Section -->
    <NavSection></NavSection>
    <!-- Call to Action Section -->
    <CallToActionSection></CallToActionSection>
    <!-- Courses Section -->
    <CoursesSection></CoursesSection>
    <!-- Events Section -->
    <EventsSection></EventsSection>
    <!-- Membership Section -->
    <MembershipSection></MembershipSection>
    <!-- Numbers Section -->
    <NumbersSection></NumbersSection>
    <!-- Form Section -->
    <ContactUsSection></ContactUsSection>
    <!-- Footer Section -->
    <FooterSection></FooterSection>

  </div>
</template>

<script>
import NavSection from '@/components/NavSection/NavSection.vue'
import CallToActionSection from '@/components/CallToActionSection/CallToActionSection.vue'
import CoursesSection from '@/components/CoursesSection/CoursesSection.vue'
import EventsSection from '@/components/EventsSection/EventsSection.vue'
import MembershipSection from '@/components/MembershipSection/MembershipSection.vue'
import NumbersSection from '@/components/NumbersSection/NumbersSection.vue'
import ContactUsSection from '@/components/ContactUsSection/ContactUsSection.vue'
import FooterSection from '@/components/FooterSection/FooterSection.vue'
// @ is an alias to /src

export default {
  name: 'HomeView',
  components: {
    NavSection,
    CallToActionSection,
    CoursesSection,
    EventsSection,
    MembershipSection,
    NumbersSection,
    ContactUsSection,
    FooterSection
  }
}
</script>