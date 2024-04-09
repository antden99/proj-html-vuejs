<script>
import AppFooterEl from './AppFooterEl.vue';
export default {
    name: "AppFooter",

    components: {
        AppFooterEl: AppFooterEl,
    },
    data() {

        return {
            footerLists: [
                {
                    title: "GET STARTED",
                    el_1: "Resources",
                    el_2: "Tutorials",
                    el_3: "Examples",
                    el_4: "Docs"
                },
                {
                    title: "ABOUT",
                    el_1: "Stories",
                    el_2: "Community",
                    el_3: "Blog",
                    el_4: "Brand Assets"
                },
                {
                    title: "FEATURES",
                    el_1: "Overview",
                    el_2: "Design",
                    el_3: "Code",
                    el_4: "Collaborate"
                },
                {
                    title: "QUICK LINKS",
                    el_1: "Stories",
                    el_2: "Community",
                    el_3: "Blog",
                    el_4: "Brand Assets"
                },
            ]
        }
    }
}

</script>

<template>

    <footer>
        <div class="container bottomBord">
            <div class="row">
                <AppFooterEl v-for="el in footerLists" :title="el.title" :el_1="el.el_1" :el_2="el.el_2" :el_3="el.el_3"
                    :el_4="el.el_4"></AppFooterEl>
                <div class="col_input">
                    <div class="title"><strong>SUBSCRIBE TO NEWSLETTER</strong></div>

                    <div><input type="email" placeholder="Email"></div>
                    <div><button>SUBSCRIBE</button></div>

                </div>
            </div>
        </div>
        <div class="container">
            <div class="final_foot">
                <div><img src="/src/assets/img/anime-whitelogo-300x89.png" alt=""></div>
                <div class="copyR">&copy; Anime Tech, Theme by HasnainDEV</div>
            </div>
        </div>

    </footer>

</template>

<style scoped>
.container {
    width: 80%;
    max-width: 1200px;
    margin: auto;
    height: 100%;
}

.bottomBord {
    border-bottom: 1px solid white;
    padding-bottom: 50px;
}

footer {
    background-color: red;
    padding-top: 50px;
    padding-bottom: 55px;
}

.row {
    display: flex;
    flex-wrap: wrap;
}

.col_input {
    flex-grow: 1;
    color: white;
}

input {
    width: 100%;
    height: 45px;
    border-radius: 5px;
    border: none;
    outline: none;
}

.title {
    margin-bottom: 20px;
}

button {
    width: 100%;
    background-color: #545454;
    color: white;
    height: 45px;
    border-radius: 5px;
    border: none;
    cursor: pointer;
    margin-top: 15px;
}
.final_foot{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}
.copyR {
    color: white;
}
</style>