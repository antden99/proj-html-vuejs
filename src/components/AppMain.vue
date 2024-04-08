<script>
import AppSectionCards from './AppSectionCards.vue';
import AppSectionLifestyle from './AppSectionLifestyle.vue';

export default {
    name: "AppMain",

    components: {
        AppSectionCards: AppSectionCards,
        AppSectionLifestyle:AppSectionLifestyle
    }
}


</script>

<template>
    <main>
        <AppSectionCards></AppSectionCards>

        <AppSectionLifestyle></AppSectionLifestyle>

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






.banner {
    background-color: chocolate;
    height: 100px;
}

.featured_posts {
    height: 200px;
}
</style>