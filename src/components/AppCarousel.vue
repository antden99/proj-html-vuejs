<script>
export default {
  name: "AppCarousel",

  data() {
    return {
      carouselLists: [
        {
          img: "src/assets/img/healthy-foods.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022",
          btn: "Food",
        },
        {
          img: "src/assets/img/winter.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022",
          btn: "Fashion",

        },
        {
          img: "src/assets/img/photographers-mistakes.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022",
          btn: "Fashion",

        },
        {
          img: "src/assets/img/ideas-anime.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022",
          btn: "Culture",
          btn2: "Stories",
        },

      ],

    }
  }
}

</script>

<template>

  <div class="carosello">
    <div class="container">
      <div class="row">
        <div class="col" v-for="element in carouselLists">
          <div class="card">
            <div class="card_head"><img :src="element.img" alt=""></div>
            <div class="card_body">
              <div class="text_description"><strong>{{ element.description }}</strong></div>
              <div class="text_date">{{ element.date }}
              </div>
            </div>
          </div>
          <div class="box_button">
            <button>{{ element.btn }}</button>
            <button v-if="element.btn2">{{ element.btn2 }}</button>
          </div>
        </div>
      </div>
      <div class="controls">
        <div class="prev"><i class="fa-solid fa-chevron-left"></i></div>
        <div class="next"><i class="fa-solid fa-chevron-right"></i></div>
      </div>

    </div>
  </div>

</template>

<style scoped>
.carosello {
  width: 100%;
  background-color: var(--third-color);
  padding: 20px 0px;

}

.container {
  position: relative;
}

.controls {
  display: flex;
  justify-content: space-between;
}
.box_button{
  position: absolute;
  top: 5%;
  left: 50%;
  transform: translate(-50%, -50%);
  gap: 10px;
  display: flex;
}
button {
  padding: 4px 15px;
  border-radius: 5px;
  border: none;
  background-color: white;

  &:hover {
    cursor: pointer;
  }
}

.prev {
  color: red;
  background-color: white;
  position: absolute;
  top: 50%;
  left: 10px;
  padding: 20px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;

  &:hover {
    cursor: pointer;
  }
}

.next {
  color: red;
  background-color: white;
  position: absolute;
  top: 50%;
  right: 10px;
  padding: 20px;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;

  &:hover {
    cursor: pointer;
  }
}

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.col {
  width: calc((100% / 12) * 3 - 10px);
  height: 400px;
  position: relative;
}

.card {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}

.card_head {
  height: 350px;
}

.card_head img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 5px;
}

.card_body {
  padding: 10px;
  height: 100px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  background-color: white;
}

.text_description {
  color: var(--fourth-colors)
}

.text_date {
  color: #a7a7a7;
}
</style>