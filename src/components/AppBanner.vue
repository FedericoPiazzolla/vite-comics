<script>
export default {
  data() {
    return {}
  },
}
</script>

<template>

<section class="banner">
  <p>Content Here</p>
</section>

</template>

<style lang="scss" scoped>
  @use "../style/partials/variables" as *;

  .banner {
    background-color: $bg_banner;
    color: white;
    height: 120px;
    text-align: center;
    padding: 2rem;
  }
</style>