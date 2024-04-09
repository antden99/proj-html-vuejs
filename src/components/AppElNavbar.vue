<script>

export default {
    name: "AppEl",
    
    props: ["elNav","elFont","arrow"],
}
</script>

<template>
    <li><i :class="elFont" aria-hidden="true"></i> <a href="#">{{ elNav }}</a> <i v-if="arrow" :class="arrow"></i></li>
</template>

<style scoped>
a{
    color: var(--fourth-colors);
    text-decoration: none;
}

li{
    color: var(--fourth-colors);
    &:hover{
        cursor: pointer;
    }
}

</style>