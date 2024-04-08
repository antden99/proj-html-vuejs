<script>

import AppHeader from './components/AppHeader.vue';
import AppCarousel from './components/AppCarousel.vue';
import AppMain from './components/AppMain.vue'


export default {
  components: {
    AppHeader: AppHeader,
    AppCarousel: AppCarousel,
    AppMain:AppMain,

  },

}
</script>

<template>
  <AppHeader></AppHeader>
  <AppCarousel></AppCarousel>
  <AppMain></AppMain>
</template>

<style scoped></style>
