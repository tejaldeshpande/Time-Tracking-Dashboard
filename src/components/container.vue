<template>
  <div class="container rounded-3xl p-8 bg-primary text-white relative">
    <div class="flex items-center justify-between mb-1">
      <div class="text-lg font-bold">{{section.title}}</div>
      <img src="content/images/icon-ellipsis.svg"/>
    </div>

    <div class="flex items-center justify-between">
      <div class="text-3xl">{{section.timeframes.daily.current}}hrs</div>
      <div class="text-sm font-bold text-primary-light">Last week - {{section.timeframes.daily.previous}}hrs</div>
    </div>

    <div class="absolute w-full h-16 rounded-t-3xl inset-0 -mt-8 section-bg bg-no-repeat" :class="'bg-'+section.theme" :style="`background-image:content/images/icon-${section.theme}.svg`">
      <!-- <img class="absolute right-0 mr-4 -mt-3 section-bg" :src="`content/images/icon-${section.theme}.svg`"/> -->
    </div>
  </div>
</template>

<script>
  export default {
    name: 'container',
    props: ['section', 'background']

  }
</script>

<style lang="scss">
.section-bg{
  background-position: right 20px center;
  z-index:-1;
}

</style>