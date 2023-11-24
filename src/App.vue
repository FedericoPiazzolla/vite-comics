<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';
import AppShop from './components/AppShop.vue';
import AppSlides from './components/AppSlides.vue';

export default {

  components: {
    AppHeader,
    AppBanner,
    AppFooter,
    AppShop,
    AppSlides,
  },
  data() {
    return {}
  },

}
</script>

<template>
 <AppHeader />
 <AppBanner />
 <AppSlides />
 <AppShop />
 <AppFooter />
</template>

<style lang="scss">
  @use "./style/general.scss"
</style>
