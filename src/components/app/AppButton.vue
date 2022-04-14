<template>
  <component
    :is="to ? 'router-link' : 'button'"
    :to="to"
    :disabled="disabled"
    class="p-2 relative border-2 rounded hover transition"
    :class="[
      outline
        ? `border-${color} text-${color} hover:bg-${color} hover:text-white`
        : `hover:bg-opacity-80 bg-${color} border-${color}  text-${
            textColor || (color === 'white' ? 'black' : 'white')
          }`,
      {
        'text-xl p-3': lg,
        'text-xs': sm,
      },
    ]"
    v-bind="$attrs"
  >
    <!-- Main Content -->
    <div class="flex items-center justify-center">
      <!-- prepend slot -->
      <div class="mr-1">
        <slot name="prepend"></slot>
      </div>
      <!-- default slot -->
      <slot></slot>
      <!-- append slot -->
      <div class="ml-1">
        <slot name="append"></slot>
      </div>
    </div>
  </component>
</template>

<script>
export default {
  name: "AppButton",
  props: {
    to: { type: [String, Object], default: null },
    sm: { type: Boolean, default: false },
    lg: { type: Boolean, default: false },
    outline: { type: Boolean, default: false },
    text: { type: Boolean, default: false },
    textColor: { type: String, default: null },
    color: { type: String, default: "primary-500" },
    disabled: { type: Boolean, default: false },
  },
};
</script>

<style lang="scss" scoped></style>
