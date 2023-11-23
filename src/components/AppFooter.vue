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
      <div class="container">
        <div class="footer-list">

          <div v-for="itemList in listFooter" class="footer-list-item">
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
    </div>

    <div class="footerBottom">

      <div class="container">
        <button>SIGN-UP NOW!</button>

        <div class="social-list">
          <h3>FOLLOW US</h3>

          <ul>
            <li v-for="itemSocial in listSocial">
              <a :href="`http://${itemSocial.link}`"><img :src=getImageUrl(itemSocial.icon) :alt="`Icon of ${itemSocial.icon}`"></a>
            </li>
          </ul>

        </div>

      </div>

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
      .container {
        color: white;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .dc-bg {
          background-position: center;
          background-repeat: no-repeat;
          background-image: url(../assets/img/dc-logo-bg.png);
          background-size: cover;
          width: 50%;
          height: 400px;
          align-self: flex-end;
        }

        .footer-list {
          display: flex;
          flex-wrap: wrap;
          align-items: flex-start;
          gap: 1rem ;

          .footer-list-item {
            padding: .8rem 0;
            width: calc(100% / 3 - 1rem);

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
    }

    .footerBottom {
      height: 100px;
      background-color: $bg_footer_dark;

      .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;

        button {
          border: 2px solid $primary;
          padding: .8rem 1rem;
          background-color: $bg_footer_dark;
          color: white;
          font-weight: bolder;
        }

        .social-list {
          display: flex;
          justify-content: space-between;
          align-items: center;
          color: $primary;
            
          ul {
            display: flex;
            justify-content: space-between;
            align-items: center;
            list-style-type: none;
            gap: 1rem;
            margin-left: 1rem;
          }
        }
      }
    }
  }
</style>