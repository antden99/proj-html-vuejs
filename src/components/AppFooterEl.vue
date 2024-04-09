<script>

export default {
    name: "AppFooterEl",

    props: ["title", "el_1", "el_2", "el_3", "el_4"],
}
</script>

<template>
    <div class="col">
        <div class="title"><strong>{{ title }}</strong></div>
        <div> <a href="à">{{ el_1 }}</a></div>
        <div> <a href="à">{{ el_2 }}</a></div>
        <div> <a href="à">{{ el_3 }}</a></div>
        <div> <a href="à">{{ el_4 }}</a></div>   
    </div>
</template>

<style scoped>
.col {
    width: calc((100% / 12) * 2);
    display: flex;
    flex-direction: column;
    color: white;
    gap: 10px;
    height: 100%;
}

.title {
    margin-bottom: 10px;
}

a{
    text-decoration: none;
    color: white;

    &:hover{
        color: var(--fourth-colors);
    }
}
</style>