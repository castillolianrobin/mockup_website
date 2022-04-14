<template>
  <div
    class="bg-white border-b border-orange-500 px-6 py-3 flex justify-between items-center"
  >
    <!-- Logo -->
    <div class="flex gap-4">
      <img src="@/assets/logo.png" class="h-10" />
      <AppButton outline>Find Courses</AppButton>
    </div>
    <!-- Navigation Items -->
    <div class="flex gap-6">
      <NavBarItems
        v-for="(item, index) in navItems"
        :key="`navItem-${item.name + index}`"
      >
        {{ item.name }}
      </NavBarItems>
    </div>
    <!-- Buttons -->
    <div class="grid grid-cols-2 gap-3">
      <AppButton outline class="px-6">Login</AppButton>
      <AppButton class="">Join</AppButton>
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
