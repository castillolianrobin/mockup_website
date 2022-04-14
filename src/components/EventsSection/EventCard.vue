<template>
  <div class="rounded bg-white p-5 flex shadow">
    <img src="@/assets/events/event-1.jpg" class="h-36" />
    <div class="px-4 flex flex-col">
      <h6 class="font-bold">Lorem Ipsum Set Dolor</h6>
      <p class="my-1 text-sm text-gray-500">Jan 27, 2022</p>
      <p class="text-sm">
        Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse
        quam nihil iure reprehenderit qui in ea voluptate velit esse quam
        nihil...
      </p>
      <p class="mt-auto cursor-pointer text-sm text-orange-500 hover:text-black transition">See more</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventCard",
};
</script>

<style lang="scss" scoped></style>
