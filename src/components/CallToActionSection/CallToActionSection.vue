<template>
  <div
    id="section1"
    class="call-to-action relative bg-cover pb-28 pt-10 md:py-10 w-full flex flex-col md:flex-row gap-28 items-center justify-center bg-[url('@/assets/callToActionBg.png')]"
  >
    <div class="text-white">
      <h1 class="text-xl md:text-5xl font-semibold">Your All-in-one CPD Solution</h1>
      <h5 class="text-sm md:text-2xl mt-5">
        laudantium, totam rem aperiam, eaque ipsa <br />
        quae ab illo inventore veritatis et quasi <br />
        architecto beatae vitae dicta sunt explicabo.<br />
      </h5>
      <AppButton lg class="mt-5">View All Course</AppButton>
    </div>
    <JoinForm class="mx-5 md:w-1/3 absolute md:relative -bottom-12 md:bottom-0"></JoinForm>
  </div>
</template>

<script>
import AppButton from "../app/AppButton.vue";
import JoinForm from "./JoinForm.vue";
export default {
  components: { AppButton, JoinForm },
  name: "CallToAction",
};
</script>

<style lang="scss" scoped></style>
