
<script >
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue'
import AppCarousel from './components/AppCarousel.vue';

export default {
  components: {
    AppHeader,
    AppFooter,
    AppCarousel
  }
}

</script>

<template>
  <AppHeader />
  <AppCarousel />
  <AppFooter />
</template>

<style  lang="scss">
@use './styles/generals.scss' as *;
</style>
