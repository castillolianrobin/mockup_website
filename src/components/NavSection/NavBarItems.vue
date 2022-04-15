<template>
  <div
    class="cursor-pointer hover:text-primary-500 transition"
    :class="{ 'text-primary-500': active }"
    v-on="$listeners"
    @click="goto"
  >
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "NavBarItems",
  props: {
    sectionID: { type: String, default: null },
    currentScroll: { type: Number, default: 0 },
  },

  data() {
    return {
      scrollTop: false,
      scrollBot: false,
    };
  },

  computed: {
    active() {
      return this.scrollBot > this.currentScroll && this.scrollTop <= this.currentScroll ;
    },
  },

  methods: {
    goto() {
      if (!this.sectionID) return;
      if (this.scrollTop === false) {
        this.assignScroll();
      }
      window.scrollTo(0, this.scrollTop);
    },
    assignScroll() {
      var element = document.getElementById(this.sectionID);
      this.scrollTop = element.offsetTop;
      this.scrollBot = element.offsetTop + element.offsetHeight;
      // console.log('height', element.offsetHeight, this.scrollTop);
    }
  },

  mounted() {
    this.assignScroll();
  },
};
</script>

<style lang="scss" scoped></style>
