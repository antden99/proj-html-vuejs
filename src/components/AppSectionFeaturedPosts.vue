<script>
export default {
    name: "AppSectionFeaturedPosts",

    data() {
        return {
            listCards:
                [
                    {
                        image: "/src/assets/img/anime-fashion.webp",
                        title: "FASHION",
                        numb: "5 POSTS",
                    },
                    {
                        image: "/src/assets/img/success-story.webp",
                        title: "CULTURE",
                        numb: "2 POSTS",
                    },
                    {
                        image: "/src/assets/img/healthy-foods.webp",
                        title: "FOOD",
                        numb: "8 POSTS",
                    },
                    {
                        image: "/src/assets/img/visit-france.webp",
                        title: "LIFESTYLE",
                        numb:"3 POSTS",
                    },
                    {
                        image: "/src/assets/img/travel-alone.webp",
                        title: "STORIES",
                        numb:"5 POSTS",
                    },
                    {
                        image: "/src/assets/img/best-places.webp",
                        title: "TRAVEL",
                        numb:"6 POSTS",
                    },
                ],

            listCategories: [
                {
                    src: "/src/assets/img/ideas-anime.webp",
                    tit_st: "Live Ideas You Might Be Anime",
                    date: "December 26, 2022",
                    lorem: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperim.",
                },
                {
                    src: "/src/assets/img/visit-france.webp",
                    tit_st: "Reasons To Visti France",
                    date: "December 26, 2022",
                    lorem: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperim.",
                },
                {
                    src: "/src/assets/img/travel-alone-300x200.webp",
                    tit_st: "Traveling Alone Is Awesome",
                    date: "December 26, 2022",
                    lorem: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperim.",
                },

            ],
            indexHover: null,
        }
    },
    methods: {
    }
}
</script>

<template>
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
                <div class="col" v-for="card in listCategories">
                    <div class="card">
                        <div class="card_head"><img :src="card.src" alt=""></div>
                        <div class="card_body">
                            <div><strong>{{ card.tit_st }}</strong></div>
                            <div class="date">December 26, 2022</div>
                            <div class="margin_top">{{ card.lorem }}</div>
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
                <div class="col_2" v-for="(image, index) in listCards" @mouseenter="indexHover = index"
                    @mouseout="indexHover = null">
                    <div><img :src="image.image" alt=""></div>
                    <div class="center text_color" :class="{border : index === indexHover}">{{ image.title }} <div v-if="index === indexHover" class="numb_posts">{{ image.numb }}</div></div>
                    <div class="red_hover" v-if="index === indexHover"></div>
                </div>
            </div>
        </section>
    </section>

</template>

<style scoped>
.featured_posts {
    padding-top: 30px;
}

.image_cards {
    margin-top: 20px;

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

    &:hover {
        color: white;
        background-color: var(--primary-color);
        cursor: pointer;
    }
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

    &:hover {
        cursor: pointer;
    }

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
        background-color: var(--fourth-colors);
        cursor: pointer;
    }
}

.red_hover {
    background-color: #ac303b;
    opacity: 0.5;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    position: absolute;
    top: 0;
}

.border{
    border: 2px solid white;
    padding: 50px;
}

.numb_posts{
    font-size: 15px;
    text-align: center;
}
</style>