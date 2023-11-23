<script>
  export default {
    data() {
      return {
        shopElem: [
          {
            url: "digital-comics",
            title: "DIGITAL COMICS",
          },
          {
            url: "merchandise",
            title: "DC MERCHANDISE",
          },
          {
            url: "subscriptions",
            title: "SUBSCRIPTIONS",
          },
          {
            url: "shop-locator",
            title: "COMIC SHOP LOCATOR",
          },
          {
            url: "dc-power-visa",
            title: "DC POWER VISA",
          },
          
        ]
      }
    },
    methods: {
      getImageUrl(imgName) {
        return new URL(`../assets/img/buy-comics-${imgName}.png`, import.meta.url).href;
      }
    }
  }
</script>

<template>

  <section>

    <div class="container">

      <div class="img-container" v-for="item in shopElem">
        <img :src=getImageUrl(item.url) :alt="`icon of ${item.title}`">
        <h5>{{ item.title }}</h5>
      </div>

    </div>

  </section>

</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

  section {
    background-color: $primary;

    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 150px;
      padding: 0 2rem;

      .img-container{
        color: white;
        display: flex;
        align-items: center;
        gap: .5rem;

        img {
          width: 25%;
        }
      }
    }
  }
</style>