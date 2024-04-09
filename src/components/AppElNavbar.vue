<script>

export default {
    name: "AppEl",

    props: ["elNav", "elFont", "arrow"],
}
</script>

<template>
    <li> <a href="#"><i :class="elFont" aria-hidden="true"></i>{{ elNav }} <i v-if="arrow" :class="arrow"></i></a></li>
</template>

<style scoped>
a {
    color: var(--fourth-colors);
    text-decoration: none;
    &:hover {
        cursor: pointer;
        color: var(--primary-color);
    }
}

i {
    margin: 0px 5px;
}
</style>