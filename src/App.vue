
<script >
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue'
import AppCarousel from './components/AppCarousel.vue';
import AppSearchCar from './components/AppSearchCar.vue';

export default {
  components: {
    AppHeader,
    AppFooter,
    AppCarousel,
    AppSearchCar,
  }
}

</script>

<template>
  <AppHeader />
  <AppCarousel />
  <AppSearchCar />
  <AppFooter />
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
