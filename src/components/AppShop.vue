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
            url: "",
            title: "COMIC SHOP LOCATOR",
          },
          {
            url: "",
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

</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;


</style>