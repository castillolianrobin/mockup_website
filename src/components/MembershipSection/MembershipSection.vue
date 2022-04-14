<template>
  <div class="p-10 py-20">
    <div class="text-center">
      <h2 class="text-2xl font-semibold">Memberships</h2>
      <h5 class="mt-1 font-light">Join Accredited Professional Organizations in your field</h5>

      <div class="mt-10 grid md:grid-cols-2 gap-4">
        <MembershipCard :img="require('@/assets/memberships/membership-1.jpg')"></MembershipCard>
        <div class="flex flex-col gap-4">
          <MembershipCard :img="require('@/assets/memberships/membership-2.jpg')"></MembershipCard>
          <MembershipCard :img="require('@/assets/memberships/membership-3.jpg')"></MembershipCard>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import MembershipCard from './MembershipCard.vue'
  export default {
  components: { MembershipCard },
    name: 'MembershipSection',
  }
</script>

<style lang="scss" scoped>

</style>