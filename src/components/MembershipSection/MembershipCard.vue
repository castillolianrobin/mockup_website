<template>
  <div
    class="relative p-4 text-white min-h-[200px]"
  >
    <img :src="img" class="absolute top-0 left-0 h-full w-full object-cover shadow-[inset_0_-70px_30px_-10px_rgba(0,0,0,0.3)]" />
    <div class="relative z-20 flex flex-col justify-end items-start h-full w-full">
      <h3 class="font-bold">ARCPP Membership Renewal for Registered Nurse</h3>
      <p class="text-sm">Php 750.00</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MembershipCard",
  props: {
    img: String,
  }
};
</script>

<style lang="scss" scoped></style>
