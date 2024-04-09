<script>
import AppSectionCards from './AppSectionCards.vue';
import AppSectionLifestyle from './AppSectionLifestyle.vue';
import AppSectionBanner from './AppSectionBanner.vue';


export default {
    name: "AppMain",

    components: {
        AppSectionCards: AppSectionCards,
        AppSectionLifestyle: AppSectionLifestyle,
        AppSectionBanner: AppSectionBanner,

    },

    data() {
        return {
            listCards:
                [
                    {
                        image: "/src/assets/img/anime-fashion.webp",
                        title: "FASHION"
                    },
                    {
                        image: "/src/assets/img/success-story.webp",
                        title: "CULTURE"
                    },
                    {
                        image: "/src/assets/img/healthy-foods.webp",
                        title: "FOOD"
                    },
                    {
                        image: "/src/assets/img/visit-france.webp",
                        title: "LIFESTYLE"
                    },
                    {
                        image: "/src/assets/img/travel-alone.webp",
                        title: "STORIES"
                    },
                    {
                        image: "/src/assets/img/best-places.webp",
                        title: "TRAVEL"
                    },
                ],
        }
    }
}


</script>

<template>
    <main>
        <AppSectionCards></AppSectionCards>

        <AppSectionLifestyle></AppSectionLifestyle>

        <AppSectionBanner></AppSectionBanner>


        <section class="featured_posts">
            <div class="container ">
                <div class="d_flex distance">
                    <div>
                        <h2>FEATURED POSTS</h2>
                    </div>
                    <div>
                        <i class="fa-solid fa-chevron-left"></i>
                        <i class="fa-solid fa-chevron-right"></i>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                        <div class="card">
                            <div class="card_head"><img src="/src/assets/img/ideas-anime.webp" alt=""></div>
                            <div class="card_body">
                                <div><strong>Live Ideas You Might Be Anime</strong></div>
                                <div class="date">December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                                    Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                                <div class="btn_read">Read More</div>
                            </div>
                        </div>
                    </div>
                    <div class="col">
                        <div class="card">
                            <div class="card_head"><img src="/src/assets/img/visit-france.webp" alt=""></div>
                            <div class="card_body">
                                <div><strong>Reasons To Visti France</strong></div>
                                <div class="date">December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                                    Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                                <div class="btn_read">Read More</div>
                            </div>
                        </div>
                    </div>
                    <div class="col">
                        <div class="card">
                            <div class="card_head"><img src="/src/assets/img/travel-alone-300x200.webp" alt=""></div>
                            <div class="card_body">
                                <div><strong>Traveling Alone Is Awesome</strong></div>
                                <div class="date">December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit.
                                    Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                                <div class="btn_read">Read More</div>

                            </div>
                        </div>
                    </div>
                </div>


                <section class="youtube_videos">
                    <div class="uploaded">
                        <div class="play"><i class="fa-brands fa-youtube"></i></div>
                    </div>
                    <div class="upload">
                        antonio
                    </div>
                </section>


            </div>
            <section class="image_cards">
                <div class="row">
                    <div class="col_2" v-for="image in listCards">
                        <img :src="image.image" alt="">
                        <div class="center text_color">{{ image.title }}</div>
                    </div>
                </div>
            </section>
        </section>
    </main>



</template>

<style scoped>
.featured_posts {
    padding-top: 30px;
}

.distance {
    justify-content: space-between;
    padding-bottom: 22px;
}

.date {
    color: #7e7e7e;
}

.d_flex {
    display: flex;
}

.container {
    width: 80%;
    max-width: 1200px;
    margin: auto;
    height: 100%;
}

h2 {
    color: #515554;
}

.container .d_flex.distance>div:last-child i {
    width: 30px;
    height: 30px;
    font-size: 20px;
    background-color: var(--fourth-colors);
    color: white;
    text-align: center;
    line-height: 30px;
    border-radius: 50%;
    margin-left: 10px;
}

.card_head {

    img {
        width: 100%;
        border-radius: 10px;
    }

}

.row {
    display: flex;
    gap: 15px;

    .col {
        width: calc((100% / 12) * 4 - 15px);
    }
}

.card_body {
    background-color: #f3f3f3;
    text-align: center;
    height: 180px;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
}

strong {
    color: #444444;
}

.margin_top {
    margin-top: 10px;
}

.uploaded {
    width: 840px;
    height: 550px;
    background-image: url("/src/assets/img/sddefault.webp");
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;


    & .play {
        position: absolute;
        top: 270px;
        left: 400px;
        width: 150px;
    }
}

.upload {
    flex-grow: 1;
}

.youtube_videos {
    display: flex;
}

i {
    color: red;
    font-size: 80px;

}

.col_2 {
    width: calc((100% / 12) * 6);
    position: relative;

    & img {
        width: 100%;
        border-radius: 10px;
    }

    & .text_color {
        color: white;
        font-size: 30px;
    }

    & .center {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
    }
}

.btn_read {
    padding: 5px 20px;
    background-color: var(--primary-color);
    color: white;
    border-radius: 20px;
    margin-top: 10px;

    &:hover {

        cursor: pointer;
    }
}
</style>