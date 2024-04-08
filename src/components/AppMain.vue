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
                                <div>December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                            </div>
                        </div>
                    </div>
                    <div class="col">
                        <div class="card">
                            <div class="card_head"><img src="/src/assets/img/visit-france.webp" alt=""></div>
                            <div class="card_body">
                                <div><strong>Reasons To Visti France</strong></div>
                                <div>December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                            </div>
                        </div>
                    </div>
                    <div class="col">
                        <div class="card">
                            <div class="card_head"><img src="/src/assets/img/travel-alone-300x200.webp" alt=""></div>
                            <div class="card_body">
                                <div><strong>Traveling Alone Is Awesome</strong></div>
                                <div>December 26, 2022</div>
                                <div class="margin_top">Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus vero aperiam ab
                                    consectetur voluptate asperiores.</div>
                                
                            </div>
                        </div>
                    </div>
                </div>
            </div>

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

i {
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

img {
    width: 100%;
    border-radius: 10px;
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

.margin_top{
    margin-top: 10px;
}
</style>