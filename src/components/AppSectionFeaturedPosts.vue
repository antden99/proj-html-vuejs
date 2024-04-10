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
                        numb: "3 POSTS",
                    },
                    {
                        image: "/src/assets/img/travel-alone.webp",
                        title: "STORIES",
                        numb: "5 POSTS",
                    },
                    {
                        image: "/src/assets/img/best-places.webp",
                        title: "TRAVEL",
                        numb: "6 POSTS",
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
            slides: [
                {
                    image: 'src/assets/img/sddefault.webp',
                    title: 'Overlord Season 4-Official Trailer 3 | AniTv',

                }, {
                    image: 'src/assets/img/season_2.jpg',
                    title: 'Rent a Girlfriend Season 2-Official Trailer | AniTv',

                }, {
                    image: 'src/assets/img/trailer_3.jpeg',
                    title: 'Unkle from Another World -Official Trailer | AniTv',

                }, {
                    image: 'src/assets/img/trailer_4.jpg',
                    title: 'Prima Doll -Official Trailer | AniTv',

                }, {
                    image: 'src/assets/img/trailer_5.jpg',
                    title: "Shoot! Goal To The Future-Official Trailer | AniTv",

                },
            ],
        }
    },
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
                    <div class="line_episode">
                        <div class="d_flex i_center"><img src="/src/assets/img/channels4_profile.jpg" alt="" class="logo_tv">
                            <div>Overlord Season 4 - Official 3 | AniTV</div></div>
                        <div class="d_flex ">
                            <div class="font_i"><i class="fa-solid fa-clock" ></i>
                                <div>Guarda di più</div>
                            </div>
                            <div class="font_i"><i class="fa-solid fa-share"></i>
                                <div>Condividi</div>
                            </div>
                        </div>
                    </div>
                    <div >
                            <button class="btn_youtube">Guarda su <i class="fa-brands fa-youtube"></i>YouTube</button>
                        </div>
                    <img src="/src/assets/img/sddefault.webp" alt="">
                    <div class="play"><i class="fa-brands fa-youtube"></i></div>
                </div>
                <div class="upload">
                    <div class="play_video">
                        <div><i class="fa-solid fa-play"></i></div>
                        <div>Video PlayList <div>1/7</div>
                        </div>
                    </div>
                    <div v-for="(n, index) in slides" class="single_video">
                        <div class="index_bord">{{ index }}</div>
                        <div><img :src="n.image" alt="" class="min_img"></div>
                        <div class="hover_title">{{ n.title }}</div>
                    </div>
                </div>
            </section>


        </div>
        <section class="image_cards">
            <div class="row">
                <div class="col_2" v-for="image in listCards">
                    <div><img :src="image.image" alt=""></div>
                    <div class="center text_color border">
                        {{ image.title }}
                        <div class="numb_posts">{{ image.numb }}</div>
                    </div>
                    <div class="red_hover"></div>
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

.i_center{
    align-items: center;
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
    object-fit: cover;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;

    & .play {
        width: 150px;
        position: absolute;
    }

    & img {
        width: 100%;
    }

    & .logo_tv {
        border-radius: 50%;
        object-fit: cover;
        max-width: 70px;
    }
}

.upload {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
}

.line_episode {
    position: absolute;
    top: 0;
    left: 0;
    color: white;
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
}

.youtube_videos {
    display: flex;
}

.play {
    color: red;
    font-size: 80px;
}
.col_2 {
    width: calc((100% / 12) * 12);
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

.col_2:hover .red_hover {
    background-color: #ac303b;
    opacity: 0.5;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    position: absolute;
    top: 0;
}

.col_2:hover .border {
    border: 2px solid white;
    padding: 50px;
}

.numb_posts {
    display: none;
}

.col_2:hover .numb_posts {
    font-size: 15px;
    text-align: center;
    display: block;
}

.play_video {
    display: flex;
    flex-grow: 1;
    background-color: #444444;
    color: white;
    border: 1px solid;
    align-items: center;
    font-size: 20px;
    border-radius: 5px;

    & i {
        font-size: 20px;
        color: white;
        margin-right: 10px;
    }
}

.min_img {
    max-width: 100px;
    min-height: 80px;
    border-radius: 10px;
    object-fit: cover;
}

.single_video {
    flex-grow: 1;
    border-bottom: 1px solid;
    display: flex;
    align-items: center;
    border-radius: 5px;

    &:hover {
        cursor: pointer;


        .index_bord {
            background-color: var(--primary-color);
        }

        .hover_title {
            color: var(--primary-color);

        }
    }


}

.index_bord {
    padding: 10px;
    background-color: var(--fourth-colors);
    color: white;
    border-radius: 5px;
    margin: 5px;
}

.font_i {
    font-size: 20px;
    color: white;
    text-align: center;
}

.m_left{
    margin-left: auto;
}

.btn_youtube{
    color: white;
    padding: 10px 20px;
    background-color:#121112;
    position: absolute;
    bottom: 0;
    left: 0;
    outline: none;
    border: none;
    border-radius: 5px;
    font-size: 20px;
    &:hover{
        cursor: pointer;

    }
}
</style>