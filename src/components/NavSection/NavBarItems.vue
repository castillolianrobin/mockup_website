<template>
  <div class="cursor-pointer hover:text-primary-500 transition">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'NavBarItems',
    props: {
      active: { type: Boolean, default: false },
    }
  }
</script>

<style lang="scss" scoped>

</style>