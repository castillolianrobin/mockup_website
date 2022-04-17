<template>
  <div class="bg-primary-100 p-3 md:py-10 md:p-8 gap-3 flex flex-col shadow-md">
    <h5 class="text-center font-semibold md:text-2xl">Join Us Free!</h5>
    <div class="hidden md:flex flex-col gap-3">
      <AppTextField
        label="First Name"
        placeholder="Enter First Name"
      ></AppTextField>
      <AppTextField
        label="Last Name"
        placeholder="Enter Last Name"
      ></AppTextField>
      <AppTextField label="Email" placeholder="Enter Email"></AppTextField>
      <AppTextField
        label="Password"
        type="password"
        placeholder="Enter 8 or 10 characters"
      ></AppTextField>
      <p>
        By signing up, you agree to our
        <router-link to="#" class="text-orange-500">Terms of Use</router-link> and
        <router-link to="#" class="text-orange-500">Privacy Policy</router-link>.
      </p>
    </div>
    <div class="grid grid-cols-2 gap-3">
      <AppButton outline class="text-xs md:text-base">Join as Professional</AppButton>
      <AppButton class="text-xs md:text-base">Join as Professional</AppButton>
    </div>
    <p class="hidden md:block text-center text-gray-500">or create an account using</p>
    <div class="hidden md:grid grid-cols-2 gap-3">
      <AppButton color="blue-900">
        <img src="@/assets/facebookLogo.png" class="w-4 mr-2" />
        Facebook
      </AppButton>
      <AppButton color="blue-600">
        <img
          src="https://cdn-icons-png.flaticon.com/512/2991/2991148.png"
          class="bg-white rounded w-4 mr-2 p-0.5"
        />
        Google
      </AppButton>
    </div>
  </div>
</template>

<script>
import AppButton from "../app/AppButton.vue";
import AppTextField from "../app/AppTextField.vue";
export default {
  components: { AppTextField, AppButton },
  name: "JoinForm",
};
</script>

<style lang="scss" scoped></style>
