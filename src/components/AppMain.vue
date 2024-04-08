<script>
export default {
    name: "AppMain",
}

</script>

<template>
    <main>
        <section class="cards">
            <div class="container">
                <div class="first_card">
                    <div class="card">
                        <img src="/src/assets/img/anime-fashion.webp" alt="">
                        <div class="box_button">
                            <button>Fashion</button>
                            <button>Lifestyle</button>
                        </div>
                        <div class="box_info">
                            <div class="first">
                                <div><i class="fa-solid fa-user"></i> demo </div>
                                <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                            </div>
                            <div>Fashion Trend Now a Days</div>
                        </div>

                    </div>
                    <div class="card">
                        <img src="/src/assets/img/travel-alone-300x200.webp" alt="">
                        <div class="box_button">
                            <button>Stories</button>
                            <button>Travel</button>
                        </div>
                        <div class="box_info">
                            <div class="first">
                                <div><i class="fa-solid fa-user"></i> demo </div>
                                <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                            </div>
                            <div>Fashion Trend Now a Days</div>
                        </div>
                    </div>
                </div>
                <div class="second_card">
                    <img src="/src/assets/img/best-places.webp" alt="" class="img">
                    <div class="box_button">
                        <button>Lifestyle</button>
                        <button>Stories</button>
                        <button>Travel</button>

                    </div>
                    <div class="box_info">
                        <div class="first">
                            <div><i class="fa-solid fa-user"></i> demo </div>
                            <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                        </div>
                        <div>Fashion Trend Now a Days</div>
                    </div>
                </div>
                <div class="third_card">
                    <div class="card">
                        <img src="/src/assets/img/music-love.webp" alt="">
                        <div class="box_button">
                            <button>Culture</button>
                            <button>Lifestyle</button>
                        </div>
                        <div class="box_info">
                            <div class="first">
                                <div><i class="fa-solid fa-user"></i> demo </div>
                                <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                            </div>
                            <div>Fashion Trend Now a Days</div>
                        </div>
                    </div>
                    <div class="card">
                        <img src="/src/assets/img/visit-france.webp" alt="">
                        <div class="box_button">
                            <button>Lifestyle</button>
                            <button>Travel</button>
                        </div>
                        <div class="box_info">
                            <div class="first">
                                <div><i class="fa-solid fa-user"></i> demo </div>
                                <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                            </div>
                            <div>Fashion Trend Now a Days</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section class="lifestyle_stories">
            <div class="container">
                Storie
            </div>
        </section>

        <section class="banner">
            <div class="container">
                Banner
            </div>

        </section>

        <section class="featured_posts">
            <div class="container ">
                Posts


            </div>

        </section>
    </main>



</template>

<style scoped>
.cards {
    margin: 10px 0px;

    & .container {
        display: flex;


        .first_card {
            width: 25%;
            display: flex;
            flex-direction: column;
        }

        .second_card {
            width: 50%;
            text-align: center;
            position: relative;

            & .box_button {
                position: absolute;
                top: 10px;
                left: 180px;
                display: flex;
                gap: 10px;

                & button {
                    padding: 4px 15px;
                    border-radius: 10px;
                    border: none;

                    &:hover {
                        cursor: pointer;
                    }
                }
            }

            .box_info {
                color: white;
                position: absolute;
                bottom: 5px;
                left: 200px;
                font-size: 15px;

                & .first {
                    display: flex;
                }
            }

        }

        .third_card {
            width: 25%;
            text-align: end;
            display: flex;
            flex-direction: column;
        }
    }
}

.lifestyle_stories {
    background-color: blueviolet;
    height: 200px;
}

.banner {
    background-color: chocolate;
    height: 100px;
}

.featured_posts {
    height: 200px;
}

.container {
    width: 80%;
    max-width: 1200px;
    margin: auto;
    height: 100%;
}

.identity {
    width: 100%;
    background-color: bisque;
}

img {
    max-width: 100%;
    border-radius: 10px;
}

.img {
    width: 95%;
    height: 100%;
}

.card {
    position: relative;
}

.box_button {
    position: absolute;
    top: 10px;
    left: 70px;
    display: flex;
    gap: 10px;

    & button {
        padding: 4px 15px;
        border-radius: 10px;
        border: none;

        &:hover {
            cursor: pointer;
        }
    }
}

.box_info {
    color: white;
    position: absolute;
    bottom: 5px;
    left: 60px;
    font-size: 15px;

    & .first {
        display: flex;
    }
}
</style>