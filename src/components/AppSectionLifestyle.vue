<script>
export default {
    name: "AppSectionLifestyle",

    data(){
        return{
            colLists:[
                {
                    src:"/src/assets/img/success-story.webp",
                    btn:"Stories",
                    desc: "Traveling Alone Is Awesome",
                },
                {
                    src:"/src/assets/img/best-places.webp",
                    btn:"Lifestyle",
                    desc: "Places For A Road Trip",
                },
                {
                    src:"/src/assets/img/music-love.webp",
                    btn:"Culture",
                    desc: "Music The Love Of My Life",
                },

            ]
        }
    }
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
                    <div class="d_flex b_line center" v-for="el in colLists">
                        <div class="p_relative">
                            <img :src="el.src" alt="" class="right_img">
                            <button class="p_absolute">{{ el.btn }}</button>
                        </div>
                        <div class="margin_left">
                            <div class="font">
                                <div><i class="fa-solid fa-user"></i> demo <i class="fa-regular fa-calendar-days"></i>
                                    December 25,2022</div>
                                <div><strong>{{ el.desc }}</strong></div>
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

.item_2 > div:nth-child(2){
    border-top: 1px solid;
    padding: 20px 0px;
    border-bottom: 1px solid;
}

.item_2 > div:nth-child(1){
   margin-bottom: 20px;
}

.item_2 > div:nth-child(3){
   margin-top: 20px;
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

.p_relative{
    position: relative;
}

.p_absolute{
    position: absolute;
    top: 2px;
    left: 2px;
}

strong:hover{
    color: var(--primary-color);
}
</style>