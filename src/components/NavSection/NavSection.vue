<template>
  <div
    class="sticky top-0 left-0 w-full z-50 bg-white border-b border-orange-500 px-6 py-3 flex justify-between items-center"
  >
    <!-- Logo -->
    <div class="hidden md:flex gap-4">
      <img src="@/assets/logo.png" class="h-10" />
      <AppButton outline>Find Courses</AppButton>
    </div>
    <!-- Navigation Icon -->
    <div class="md:hidden">
      <svg
        width="25"
        height="15"
        viewBox="0 0 25 15"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        @click="showNav = !showNav"
      >
        <path
          fill-rule="evenodd"
          clip-rule="evenodd"
          d="M0 2.5V0H25V2.5H0ZM0 6.25V8.75H25V6.25H0ZM0 12.5V15H25V12.5H0Z"
          fill="#2F80ED"
        />
      </svg>
    </div>
    <!-- Navigation Items -->
    <div
      class="flex flex-col md:flex-row gap-6 absolute top-12 md:top-0 md:relative shadow-md md:shadow-none bg-white p-4"
      :class="{ 'hidden md:flex': !showNav, 'flex': showNav }"
      @click="showNav = false"
    >
      <NavBarItems
        v-for="(item, index) in navItems"
        :key="`navItem-${item.name + index}`"
      >
        {{ item.name }}
      </NavBarItems>
    </div>
    <!-- Buttons -->
    <div class="grid md:grid-cols-2 gap-3">
      <AppButton outline class="px-6">Login</AppButton>
      <AppButton class="hidden md:block">Join</AppButton>
    </div>
  </div>
</template>

<script>
import AppButton from "../app/AppButton.vue";
import NavBarItems from "./NavBarItems.vue";
export default {
  name: "NavBar",
  components: {
    AppButton,
    NavBarItems,
  },

  data() {
    return {
      showNav: false,
      navItems: [
        { name: "Home", active: false },
        { name: "Courses", active: false },
        { name: "Events", active: false },
        { name: "Memberships", active: false },
        { name: "Contact Us", active: false },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
