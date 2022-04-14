<template>
  <div>
    <label v-if="label" class="block">{{ label }}</label>
    <input
      :value="value"
      :type="type"
      class="p-1.5 w-full border hover:border-primary-500 focus:border-primary-700 translate-x-0 outline-none"
      @input="changeValue"
      v-bind="$attrs"
    />
  </div>
</template>

<script>
export default {
  name: "AppTextField",
  props: {
    label: { type: String, default: null },
    value: { type: String, default: null },
    type: { type: String, default: "text" },
  },
  methods: {
    changeValue(event) {
      this.$$emit("input", event.target.value);
    },
  },
};
</script>

<style lang="scss" scoped></style>
