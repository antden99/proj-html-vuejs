<script>
export default {
    name: "AppSectionLifestyle",
}
</script>

<template>
    <section class="lifestyle_stories">
        <div class="container">
            <div class="d_flex distance">
                <div>
                    <h2>LIFESTYLE & STORIES</h2>
                </div>
                <div>
                    <button class="btn">ALL</button>
                    <button class="btn">LIFESTYLE</button>
                    <button class="btn">STORIES</button>
                </div>
            </div>
            <div class="d_flex">
                <div class="item_1">
                    <img src="/src/assets/img/success-story.webp" alt="">
                    <button>
                        Culture
                    </button>
                    <div class="box_info">
                        <div class="first">
                            <div><i class="fa-solid fa-user"></i> demo </div>
                            <div><i class="fa-regular fa-calendar-days"></i> December 25,2022</div>
                        </div>
                        <div><strong>Fashion Trend Now a Days</strong></div>
                    </div>
                </div>
                <div class="item_2">
                    <div class="d_flex b_line center">
                        <div>
                            <img src="/src/assets/img/travel-alone-300x200.webp" alt="" class="right_img">
                        </div>
                        <div class="margin_left">
                            <div class="font">
                                <div><i class="fa-solid fa-user"></i> demo <i class="fa-regular fa-calendar-days"></i>
                                    December 25,2022</div>
                                <div><strong>Traveling Alone Is Awesome</strong></div>
                            </div>
                        </div>
                    </div>
                    <div class="d_flex b_line center">
                        <div>
                            <img src="/src/assets/img/best-places.webp" alt="" class="right_img">
                        </div>
                        <div class="margin_left">
                            <div class="font">
                                <div><i class="fa-solid fa-user"></i> demo <i class="fa-regular fa-calendar-days"></i>
                                    December 25,2022</div>
                                <div><strong>Traveling Alone Is Awesome</strong></div>
                            </div>
                        </div>
                    </div>
                    <div class="d_flex center">
                        <div>
                            <img src="/src/assets/img/music-love.webp" alt="" class="right_img">
                        </div>
                        <div class="margin_left">
                            <div class="font">
                                <div><i class="fa-solid fa-user"></i> demo <i class="fa-regular fa-calendar-days"></i>
                                    December 25,2022</div>
                                <div><strong>Traveling Alone Is Awesome</strong></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
.lifestyle_stories {
    margin-top: 50px;
    margin-bottom: 60px;
    & h2 {
        color: #515554;
    }
}

.distance {
    justify-content: space-between;
    padding-bottom: 22px;
}

.btn {
    background-color: #515554;
    color: white;
    padding: 10px 15px;
    border: none;
    border-radius: 5px;
    margin-left: 10px;
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


.item_1 {
    position: relative;
    width: 730px;

    & button {
        position: absolute;
    }
}

.item_2 {
    flex-grow: 1;
    margin-left: 30px;
}

img {
    width: 100%;
    height: 440px;
    border-radius: 10px;
    opacity: 0.8;
}


button {
    padding: 4px 15px;
    border-radius: 5px;
    border: none;
    background-color: white;
    top: 10px;
    left: 10px;

    &:hover {
        cursor: pointer;
    }
}

.box_info {
    color: white;
    position: absolute;
    bottom: 10px;
    left: 10px;
    font-size: 20px;

    & .first {
        display: flex;
    }
}

.right_img {
    width: 180px;
    height: 120px;
}

.b_line {
    border-bottom: 1px solid black;
    padding-bottom: 22px;
}

.item_2>div:nth-child(2) {
    padding-top: 22px;
}


.margin_left {
    margin-left: 20px;

    & .font {
        font-size: 17px;
        color: #555555;
    }
}

.center {
    align-items: center;
}
</style>