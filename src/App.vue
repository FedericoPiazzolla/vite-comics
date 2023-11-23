<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';
import AppShop from './components/AppShop.vue';

export default {

  components: {
    AppHeader,
    AppBanner,
    AppFooter,
    AppShop,
  },
  data() {
    return {}
  },

}
</script>

<template>
 <AppHeader />
 <AppBanner />
 <AppShop />
 <AppFooter />
</template>

<style lang="scss">
  @use "./style/general.scss"
</style>
