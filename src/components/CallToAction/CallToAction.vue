<template>
  <div
    class="call-to-action bg-cover py-6 flex gap-28 items-center justify-center"
  >
    <div class="text-white">
      <h1 class="text-5xl font-semibold">Your All-in-one CPD Solution</h1>
      <h5 class="text-2xl mt-5">
        laudantium, totam rem aperiam, eaque ipsa <br>
        quae ab illo inventore veritatis et quasi <br> 
        architecto beatae vitae dicta sunt explicabo.<br>
      </h5>
      <AppButton lg class="mt-3">View All Course</AppButton>
    </div>
    <JoinForm class="w-1/3"></JoinForm>
  </div>
</template>

<script>
import AppButton from '../app/AppButton.vue';
import JoinForm from './JoinForm.vue';
export default {
  components: { AppButton, JoinForm, },
  name: "CallToAction",
};
</script>

<style lang="scss" scoped>
.call-to-action {
  background-image: url("@/assets/callToActionBg.png");
}
</style>
