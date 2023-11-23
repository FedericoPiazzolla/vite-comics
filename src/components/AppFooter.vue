<script>
  export default {
    data() {
      return {
        listFooter: [
          {
            title: "DC COMICS",
            list: ["Charaters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
          },
          {
            title: "SHOP",
            list: ["Shop DC", "Shop DC Collectibles"]
          },
          {
            title: "DC",
            list: ["Terms Of Use", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshop", "CPSC Certificates", "Rating", "Shop Help", "Contact Us"]
          },
          {
            title: "SITES",
            list: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
          },
        ],
        listSocial: [
          {
            icon: "facebook",
            link: ""
          },
          {
            icon: "twitter",
            link: ""
          },
          {
            icon: "youtube",
            link: ""
          },
          {
            icon: "pinterest",
            link: ""
          },
          {
            icon: "periscope",
            link: ""
          },
        ]
      }
    },
    methods: {
      getImageUrl(imgName) {
      return new URL(`../assets/img/footer-${imgName}.png`, import.meta.url).href;
    }
    }
  }
</script>

<template>

  <footer>
    <div class="footerTop">
      <div class="footer-list">
        <div v-for="itemList in listFooter">
          <h4>{{ itemList.title }}</h4>
          <ul>
            <li v-for="item in itemList.list">
              <a href="">{{ item }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="dc-bg"></div>
    </div>

    <div class="footerBottom">

    </div>

  </footer>

</template>

<style lang="scss" scoped>  
  @use "../style/partials/variables" as *;
  
  footer {
    height: 400px;
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);

    .footerTop {
      color: white;
      display: flex;
      justify-content: space-between;

      .dc-bg {
        background-position: center;
        background-repeat: no-repeat;
        background-image: url(../assets/img/dc-logo-bg.png);
        width: 50%;
        height: 400px;
      }

      .footer-list {
        display: flex;
        padding: 2rem 0;
        gap: 1rem;

        div {
          padding: 1rem;
        }
        
        ul {
          list-style-type: none;
        }

        a {
          color: gray;
          font-size: .7rem;
          text-decoration: none;
        }
      }
    }
  }
</style>