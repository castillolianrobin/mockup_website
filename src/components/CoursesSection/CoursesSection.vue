<template>
  <div class="bg-gray-100 pt-24 pb-12 md:py-16 p-5">
    <div class="md:grid md:grid-cols-3">
      <h1 class="col-start-2 text-2xl text-center font-bold">
        Popular Courses
      </h1>
      <div class="mt-5 md:mt-0 flex justify-center md:justify-end">
        <select class="p-1">
          <option selected>All Courses</option>
          <option
            v-for="(type, index) in types"
            :key="`type-option-${index + type.name}`"
          >
            {{ type.name }}
          </option>
        </select>
      </div>
    </div>
    <!-- types -->
    <div class="mt-10 flex gap-5 justify-center">
      <h3
        v-for="(type, index) in types"
        :key="`type-${index + type.name}`"
        class="px-4 py-2 cursor-pointer hover:bg-blue-300 rounded transition"
        :class="{
          'text-white bg-blue-500 ': type.active,
        }"
      >
        {{ type.name }}
      </h3>
    </div>

    <!-- Course Cards -->
    <div class="overflow-hidden w-full">
      <div
        class="pb-4 mt-5 flex gap-4 scroll-m-0 overflow-auto scroll-smooth no-scrollbar"
      >
        <CourseCard
          v-for="(course, index) in courses"
          :key="`course-${index}`"
          :img="course.img"
          :title="course.title"
          :price="course.price"
          :stars="course.stars"
          class="flex-shrink-0 cursor-pointer"
        >
        </CourseCard>
      </div>

      <AppButton outline class="block mx-auto mt-12">View All Courses</AppButton>
    </div>
  </div>
</template>

<script>
import AppButton from '../app/AppButton.vue';
import CourseCard from "./CourseCard.vue";
export default {
  name: "CoursesSection",
  components: { CourseCard, AppButton },
  data() {
    return {
      types: [
        { name: "Agriculture", active: true },
        { name: "Architecture", active: false },
        { name: "Criminology", active: false },
        { name: "Medicine", active: false },
        { name: "Midwifery", active: false },
        { name: "Nursing", active: false },
        { name: "Veterinary Medicine", active: false },
      ],
      courses: [
        {
          img: "course-1.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 750,
          stars: 2458,
        },
        {
          img: "course-2.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 1000,
          stars: 50,
        },
        {
          img: "course-3.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 2500.50,
          stars: 120,
        },
        {
          img: "course-1.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 750,
          stars: 500,
        },
        {
          img: "course-2.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 750,
          stars: 2458,
        },
        {
          img: "course-3.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 2500.50,
          stars: 120,
        },
        {
          img: "course-3.jpg",
          title: "Lastest Updates in Small Animal Cardiology Practice",
          price: 2500.50,
          stars: 120,
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
/* Hide scrollbar for Chrome, Safari and Opera */
.no-scrollbar::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.no-scrollbar {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
  -webkit-overflow-scrolling: touch;
}
</style>
