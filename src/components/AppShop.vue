<script>
  export default {
    data() {
      return {
        shopElem: [
          {
            url: "comics-digital-comics",
            file: "png",
            title: "DIGITAL COMICS",
          },
          {
            url: "comics-merchandise",
            file: "png",
            title: "DC MERCHANDISE",
          },
          {
            url: "comics-subscriptions",
            file: "png",
            title: "SUBSCRIPTIONS",
          },
          {
            url: "comics-shop-locator",
            file: "png",
            title: "COMIC SHOP LOCATOR",
          },
          {
            url: "dc-power-visa",
            file: "svg",
            title: "DC POWER VISA",
          },
          
        ]
      }
    },
    methods: {
      getImageUrl(imgName, imgFile) {
        return new URL(`../assets/img/buy-${imgName}.${imgFile}`, import.meta.url).href;
      }
    }
  }
</script>

<template>

  <section>

    <div class="container">

      <div class="img-container" v-for="item in shopElem">
        <img :src="getImageUrl(item.url, item.file)" :alt="`icon of ${item.title}`">
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