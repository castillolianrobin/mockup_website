<template>
  <div class="px-10 md:px-44 py-20 flex flex-col md:flex-row bg-gray-100">
    <!-- get in touch -->
    <div class="md:w-2/5 md:px-10">
      <h2 class="md:text-2xl font-bold">Get In Touch</h2>
      <div class="flex flex-col gap-3 md:gap-5">
        <div class="order-3 md:order-1">
          <p class="text-orange-500 font-semibold">Phones</p>
          <p class="my-2">+63 02 500 6230</p>
        </div>
        <div class="bg-gray-200 h-0.5 w-full order-2"></div>
        <div class="order-5 md:order-3">
          <p class="text-orange-500 font-semibold">E-mail</p>
          <p class="my-2">support@icpdgateway.ph</p>
        </div>
        <div class="bg-gray-200 h-0.5 w-full order-4"></div>
        <div class="order-1 md:order-5">
          <p class="text-orange-500 font-semibold">Address</p>
          <p class="my-2">Lorem Ipsum Street, Manila PH</p>
        </div>
      </div>
    </div>
    <!-- contact form -->
    <div class="mt-10 md:mt-0 flex-grow flex-shrink flex flex-col gap-4">
      <h2 class="md:text-2xl font-bold">Contact Form</h2>
      <div class="grid md:grid-cols-2 gap-4">
        <AppTextField placeholder="Full Name"></ApptextField>
        <AppTextField placeholder="Contact Number"></ApptextField>
      </div>

      <textarea placeholder="Your Message" rows="6"></textarea>

      <div class="grid md:grid-cols-2 gap-4">
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
