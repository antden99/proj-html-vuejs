<script>
import AppElNavbar from './AppElNavbar.vue';

export default {
  name: "AppHeader",

  data() {
    return {
      elementsNavbar: [
        {
          fontA: "fa-solid fa-house",
          link: "HOME",
        },
        {
          fontA: "fa-solid fa-suitcase",
          link: "LIFESTYLE",
          arrowDown:"fa-solid fa-chevron-down",
        }, {
          fontA: "fa-solid fa-book-open-reader",
          link: "STORIES",
          arrowDown:"fa-solid fa-chevron-down",
        }, {
          fontA: "fa-solid fa-book",
          link: "PAGES",
          arrowDown:"fa-solid fa-chevron-down",
        }, {
          fontA: "fa-solid fa-user",
          link: "ABOUT US",
        },
      ],
      elementHamb : "fa-solid fa-bars",
      elementSearch : "fa-solid fa-magnifying-glass"
      
    }
  },

  components: {
    AppElNavbar: AppElNavbar,
  }
}

</script>

<template>
  <div class="item_1">
    <div class="container d_flex">
      <div class="left">
        <ul>
          <li>News Update</li>
          <li><img class="prima" src="/src/assets/img/meal-time-150x150.webp" alt=""></li>
          <li></li>
        </ul>
      </div>
      <div class="right d_flex">
        <div class="d_flex distance">
          <i class="fa-brands fa-facebook-f"></i>
          <i class="fa-brands fa-twitter"></i>
          <i class="fa-brands fa-instagram"></i>
          <i class="fa-brands fa-youtube"></i>
        </div>
        <div class="d_flex distance">
          <i class="fa-solid fa-chevron-left"></i>
          <i class="fa-solid fa-chevron-right"></i>
        </div>
      </div>
    </div>
  </div>
  <div class="item_2">
    <div class="container">
      <div class="logo">
        <img src="/src/assets/img/logo_animetech.webp" alt="">
      </div>
      <div>
        <img src="/src/assets/img/header-banner.webp" alt="" class="logo2">
      </div>
    </div>
  </div>
  <div class="item_3">
    <div class="container">

      <div class="hamburg">
        <AppElNavbar :elFont="elementHamb"></AppElNavbar>
      </div>
      <div class="menu">
        <nav>
          <AppElNavbar v-for="el in elementsNavbar" :elNav="el.link" :elFont="el.fontA" :arrow="el.arrowDown"></AppElNavbar>
        </nav>
      </div>
      <div class="search">
        <AppElNavbar :elFont="elementSearch"></AppElNavbar>
      </div>

    </div>
  </div>


</template>

<style scoped>
.container {
  width: 80%;
  max-width: 1200px;
  margin: auto;
  height: 100%;
}

.item_1 {
  background-color: var(--primary-color);
  height: 50px;

  & ul {
    display: flex;
    list-style: none;
    align-items: center;
    font-size: 30px;
    height: 100%;

    >li:first-child {
      background-color: #545453;
      height: 100%;
      color: white;
    }
  }
}

.item_3 {
  color:var(--fourth-colors);
  width: 100%;
  height: 50px;
  font-size: 30px;
}

.item_2 {
  background-color: var(--secondary-color);
  width: 100%;
  height: 118px;

  & .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}

.item_3 {
  & .container {
    display: flex;
    justify-content: space-around;

    & div {
      display: flex;
      align-items: center;
    }

    & .search {
      flex-direction: row-reverse;
      width: 25%;
      list-style: none;
    }

    & .hamburg{
      width: 25%;
      list-style: none;
    }

    & .menu{
      flex-grow: 1;
    }
  }
}

img.prima {
  height: 50px;
  aspect-ratio: 1;
  opacity: 0.7;
  margin-top: 7px;
}

img.logo {
  width: 225px;
  height: 117px;
}

img.logo2 {
  width: 715px;
  height: 90px;
  border-radius: 10px;
}

.left {
  height: 100%;
  width: 50%;
}

.right {
  flex-grow: 1;
  flex-direction: row-reverse;
  gap: 50px;
}

ul {
  display: flex;
  list-style: none;
  align-items: center;
  font-size: 30px;
  height: 100%;

  >li:first-child {
    background-color: #545453;
    height: 100%;
  }
}

.d_flex {
  display: flex;
  align-items: center;
}

.distance {
  gap: 20px;
  color: white;
}

.right>div:first-child i {
  display: inline-block;
  width: 30px;
  height: 30px;
  font-size: 20px;
  background-color: white;
  color: var(--primary-color);
  text-align: center;
  line-height: 30px;
  border-radius: 50%;
}

nav {
  display: flex;
  justify-content: space-between;
  width: 100%;
  list-style: none;
  gap: 25px;
  font-size: 15px;
}
</style>