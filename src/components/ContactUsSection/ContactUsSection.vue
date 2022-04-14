<template>
  <div class="px-44 py-20 flex bg-gray-100">
    <!-- get in touch -->
    <div class="w-2/5">
      <h2 class="text-2xl font-bold">Get In Touch</h2>
      <div class="my-5">
        <p class="text-orange-500 font-semibold">Phones</p>
        <p class="my-2">+63 02 500 6230</p>
      </div>
      <div class="bg-gray-100 h-0.5 w-full"></div>
      <div class="my-5">
        <p class="text-orange-500 font-semibold">E-mail</p>
        <p class="my-2">support@icpdgateway.ph</p>
      </div>
      <div class="bg-gray-100 h-0.5 w-full"></div>
      <div class="my-5">
        <p class="text-orange-500 font-semibold">Address</p>
        <p class="my-2">Lorem Ipsum Street, Manila PH</p>
      </div>
    </div>
    <!-- contact form -->
    <div class="flex-grow-1 flex-shrink-1 w-3/5 flex flex-col gap-4">
      <h2 class="text-2xl font-bold">Contact Form</h2>
      <div class="grid grid-cols-2 gap-4">
        <AppTextField placeholder="Full Name"></ApptextField>
        <AppTextField placeholder="Contact Number"></ApptextField>
      </div>

      <textarea placeholder="Your Message" rows="6"></textarea>

      <div class="grid grid-cols-2 gap-4">
        <AppTextField placeholder="Email Address"></AppTextField>
        <AppButton sm>Send Message</AppButton>
      </div>
    </div>
  </div>
</template>

<script>
import AppButton from '../app/AppButton.vue';
import AppTextField from "../app/AppTextField.vue";

export default {
  name: "ContactUsSection",
  components: {
    AppTextField,
    AppButton,
  },
};
</script>

<style lang="scss" scoped></style>
