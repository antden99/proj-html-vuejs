<script>
export default {
    name: "AppMain",
}

</script>

<template>
    <div>

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
    </div>

</template>

<style scoped>
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
    border: 2px dotted black;
    height: 100%;
}

.identity {
    width: 100%;
    background-color: bisque;
}
</style>