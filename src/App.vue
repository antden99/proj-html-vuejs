<script>

import AppHeader from './components/AppHeader.vue';
import AppCarousel from './components/AppCarousel.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';


export default {
  components: {
    AppHeader: AppHeader,
    AppCarousel: AppCarousel,
    AppMain:AppMain,
    AppFooter:AppFooter,

  },

}
</script>

<template>
  <AppHeader></AppHeader>
  <AppCarousel></AppCarousel>
  <AppMain></AppMain>
  <AppFooter></AppFooter>
</template>

<style scoped></style>
