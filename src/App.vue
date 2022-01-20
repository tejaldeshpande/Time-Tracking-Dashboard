<template>
  <div id="app" class="px-6 py-10 ">
    <div class="text-3xl text-primary-light text-center mb-6">Time Tracking Dashboard</div>
    <user-container class="mt-8 mb-36"></user-container>
    <div class="space-y-16">
      <container v-for="cat in categories" :key="cat.title" :section="cat"></container>
    </div>

  </div>
</template>

<script>
import categories from '../public/content/data/data.json'
import container from '@/components/container.vue'
import UserContainer from './components/user-container.vue'


export default {
  data() {
    return {
      categories: categories
    }
  },
  components: {
    container,
    UserContainer
  },
}
</script>


<style lang="scss">
html{
  background-color: hsl(226, 43%, 10%);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // color: #2c3e50;

}

</style>
