<script>
export default {
  name: "AppCarousel",

  data() {
    return {
      carouselLists: [
        {
          img: "src/assets/img/mealtime.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022"
        },
        {
          img: "src/assets/img/winter.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022"
        },
        {
          img: "src/assets/img/photographers-mistakes.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022"
        },
        {
          img: "src/assets/img/ideas-anime.webp",
          description: "The Best Healty Foods in 2022",
          date: "December 26, 2022"
        },
      ]
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
        </div>

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

.row {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  justify-content: center;
}

.col {
  width: calc((100% / 12) * 3 - 10px);
  height: 400px;
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

.text_description{
  color:var(--fourth-colors)
}

.text_date{
  color:#a7a7a7;
}
</style>