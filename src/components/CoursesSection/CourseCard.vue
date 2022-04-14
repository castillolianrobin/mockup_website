<template>
  <div class="bg-white rounded p-2 w-72 shadow-md">
    <img :src="require('@/assets/courses/' + img)" />
    <h5 class="mt-3 font-bold">{{ title }}</h5>
    <div class="mt-3 flex justify-between">
      <p class="text-gray-500">
        Php {{ price.toLocaleString("en-US", { minimumFractionDigits: 2 }) }}
      </p>
      <div class="flex items-center gap-2 text-orange-500 font-bold">
        <!-- Star Icon -->
        <svg
          width="13"
          height="13"
          viewBox="0 0 13 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M6.80421 0.795654L8.16594 4.50949H12.942L9.25173 7.50534L10.3411 11.7349L6.80964 9.25925L2.85156 12.1479L4.26227 7.50534L0.463104 4.50949H5.23913L6.80421 0.795654Z"
            fill="#FE5F06"
          />
        </svg>
        <p>{{ stars }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CourseCard",
  props: {
    img: { type: String, default: null },
    title: { type: String, default: null },
    price: { type: Number, default: null },
    stars: { type: Number, default: null },
  },
};
</script>

<style lang="scss" scoped></style>
