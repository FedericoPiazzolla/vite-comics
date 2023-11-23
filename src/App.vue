<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';
import AppFooter from './components/AppFooter.vue';

export default {

  components: {
    AppHeader,
    AppBanner,
    AppFooter,
  },
  data() {
    return {}
  },

}
</script>

<template>
 <AppHeader />
 <AppBanner />

 <AppFooter />
</template>

<style lang="scss">
  @use "./style/general.scss"
</style>
