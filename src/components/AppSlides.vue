<script>
import ProductSlides from './ProductSlides.vue';

export default {
  data() {
    return {
      comics: [
        {
          "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ]
    }
  },
  components: { ProductSlides },
}

</script>

<template>

  <section class="slides-container">

    <div class="container">
      <div class="bage">CURRENT SERIES</div>

      <div class="row">
        <div class="col" v-for="(comic, index) in comics" :key="index">
          <ProductSlides :title="comic.series" :image="comic.thumb"/>
        </div>
      </div>

      <div class="btn">
        <a href="" class="btn-slides">LOAD MORE</a>
      </div>
      
    </div>

  </section>

</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;
.slides-container {
  background-color: $bg_banner;

  .bage {
    background-color: $primary;
    display: inline-block;
    color: white;
    padding: 1rem;
    font-weight: bolder;
    font-size: 1.2rem;
    position: relative;
    top: -1.7rem;
    left: 0;
  }
  .row {
    display: flex;
    justify-content: center;
    align-items: stretch;
    flex-wrap: wrap;
    padding-top: 1.6rem;

    .col {
      width: calc(100% / 6);
      padding: 1rem;
    }
  }

  .btn {
    display: flex;
    width: 100%;
    justify-content: center;
    padding-bottom: 1rem;

    .btn-slides {
      background-color: $primary;
      text-decoration: none;
      padding: .6rem 1.6rem;
      color: white;
      font-size: .8rem;
      font-weight: bolder;
      cursor: pointer;
    }
  }
  
}
  
</style>