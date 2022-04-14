<template>
  <div class="rounded bg-white p-5 flex flex-col md:flex-row shadow">
    <img :src="img" class="h-36" />
    <div class="mt-5 md:mt-0 md:px-4 flex flex-col">
      <h6 class="font-bold">{{ title }}</h6>
      <p class="my-1 text-sm text-gray-500">{{ date }}</p>
      <p class="text-sm">
        {{ description }}
      </p>
      <p class="mt-2 md:mt-auto cursor-pointer text-sm text-orange-500 hover:text-black transition">See more</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "EventCard",

  props: {
    img: String,
    title: String,
    date: String,
    description: String,
  }
};
</script>

<style lang="scss" scoped></style>
