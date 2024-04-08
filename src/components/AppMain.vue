<script>
import AppSectionCards from './AppSectionCards.vue';
import AppSectionLifestyle from './AppSectionLifestyle.vue';
import AppSectionBanner from './AppSectionBanner.vue';


export default {
    name: "AppMain",

    components: {
        AppSectionCards: AppSectionCards,
        AppSectionLifestyle:AppSectionLifestyle,
        AppSectionBanner:AppSectionBanner,

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
                Posts
            </div>

        </section>
    </main>



</template>

<style scoped>








.featured_posts {
    height: 200px;
}
</style>