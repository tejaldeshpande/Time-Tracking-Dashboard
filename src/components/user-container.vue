<template>
  <div class="user-container rounded-3xl p-6 py-10 bg-active text-white relative">

    <div class="flex items-center justify-around">
      <img class="w-16 border-2 border-white rounded-full" src="content/images/image-jeremy.png"/>

      <div>
        <div class="text-md font-bold text-primary-light">Report for</div>
        <div class="text-2xl font-medium">Jeremy Robson</div>
      </div>

    </div>

    <div class="absolute w-full h-24 rounded-b-3xl bottom-0 left-0 bg-primary -mb-20 flex items-center" style="z-index:-1">
      <div class="flex justify-around w-full capitalize mt-4">
        <div class="text-lg text-primary-light font-bold" v-for="option in options" :key="option">{{option}}</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'user-container',
    data() {
      return {
        options: ['daily', 'weekly', 'monthly']
      }
    },

  }
</script>

<style lang="scss">


</style>