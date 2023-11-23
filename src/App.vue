<script>
import AppHeader from './components/AppHeader.vue';
import AppBanner from './components/AppBanner.vue';

export default {

  components: {
    AppHeader,
    AppBanner,
  },
  data() {
    return {}
  },

}
</script>

<template>
 <AppHeader />
 <AppBanner />
</template>

<style lang="scss">
  @use "./style/general.scss"
</style>
