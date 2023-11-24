<script>

export default {
  data() {
    return {
      navItems: [
        {
          title: "CHARACTERS",
        },
        {
          title: "COMICS",
        },
        {
          title: "MOVIES",
        },
        {
          title: "TV",
        },
        {
          title: "GAMES",
        },
        {
          title: "COLLECTIBLES",
        },
        {
          title: "VIDEOS",
        },
        {
          title: "FANS",
        },
        {
          title: "NEWS",
        },
        {
          title: "SHOP",
        },
      ],
    }
  },
}

</script>

<template>
  <header>
    <!-- Container -->
    <div class="container">

      <div class="wrapper flex">
        <div class="logoCol">
          <img src="../assets/img/dc-logo.png" alt="">
        </div>

        <div class="linkCol">
          <ul>
            <li v-for="item in navItems" :key="item.title">
              <a href="">{{ item.title }}</a>
            </li>
          </ul>
        </div>
      </div>

    </div>
    <!-- Container -->
  </header>
  
</template>

<style lang="scss" scoped>
@use "../style/partials/variables" as *;

header {
  
  .wrapper {
    height: 120px;


    &.flex {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;
    }

    .logoCol {
      
      img {
        min-width: 65px;
      }

    }

    .linkCol {
      height: 120px;


      ul {
        list-style-type: none;
        display: flex;
        align-items: center;
        height: 100%;

        li {
          font-size: .8rem;
          padding: 0 .5rem;
          cursor: pointer;
          display: flex;
          align-items: center;
          height: 100%;
          border-bottom: 3px solid transparent;

          a {
            text-decoration: none;
            color: inherit;
            
          }

          &:hover{
            border-bottom: 3px solid $primary;
          }
        }

        
      }
    }

  }
}

</style>