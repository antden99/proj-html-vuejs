<script>
import AppSectionCards from './AppSectionCards.vue';
import AppSectionLifestyle from './AppSectionLifestyle.vue';
import AppSectionBanner from './AppSectionBanner.vue';
import AppSectionFeaturedPost from './AppSectionFeaturedPosts.vue';

export default {
    name: "AppMain",

    components: {
        AppSectionCards,
        AppSectionLifestyle,
        AppSectionBanner,
        AppSectionFeaturedPost,
    },
}
</script>

<template>
    <main>
        <AppSectionCards></AppSectionCards>
        <AppSectionLifestyle></AppSectionLifestyle>
        <AppSectionBanner></AppSectionBanner>
        <AppSectionFeaturedPost></AppSectionFeaturedPost>
    </main>
</template>

<style scoped>

</style>
