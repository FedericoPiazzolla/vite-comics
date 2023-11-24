<script>
export default {
  props: {
    title: String,
    image: String,
  }
}
</script>

<template>
  <div class="card">
    <img :src="image" alt="">
    <h3>{{ title }}</h3>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.card {
  background-color: $bg_banner;
  height: 100%;
  color: wheat;

  img {
    width: 150px;
    height: 120px;
    object-fit: cover;
  }

  h3 {
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    font-size: .8rem;
    padding: .5rem;
  }
}
</style>