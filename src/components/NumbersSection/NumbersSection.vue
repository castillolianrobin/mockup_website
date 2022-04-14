<template>
  <div class="px-10 py-6 flex gap-20 justify-center bg-[url('@/assets/numbers/bg.jpg')]">
    <div v-for="(number, index) in numbers" :key="`numbers-${index}`">
      <h1 class="text-white text-4xl font-bold">{{ number.number }}</h1>
      <div class="my-4 h-1 w-10 bg-orange-500"></div>
      <p class="text-white text-sm">{{ number.title }}</p>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'NumbersSection',

    data() {
      return {
        numbers: [
          { number: '05', title: 'National Organization' },
          { number: '27', title: 'Board Professions' },
          { number: '1.5K+', title: 'Signed-up Professionals' },
          { number: '20', title: 'Sectoral Organizatons' },
          { number: 'P71.4', title: 'Average Price per Unit' },
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>