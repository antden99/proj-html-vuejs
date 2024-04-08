<script>
export default {
    name: "AppSectionBanner",
}

</script>

<template>

    <section class="banner">
        <div class="container">
            <img src="/src/assets/img/page-banner-1.webp" alt="">
        </div>
    </section>
</template>

<style scoped>
.container {
    width: 80%;
    max-width: 1200px;
    margin: auto;
    height: 100%;
    display: flex;
    align-items: center;

    & img {
        width: 100%;
        height: 90px;
        border-radius: 10px;
    }
}



.banner {
    background-color: #f3f3f3;
    height: 170px;
}
</style>