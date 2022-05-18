<script setup>
    defineProps(["name", "imgRoute"]);
</script>

<template>
<button class="card">
    <img :src="imgRoute" alt="">
    <p>{{name}}</p>
</button>
</template>

<style scoped>
    .card {
        border: none;
        background-color: #02023a00;
    }

    .card:hover p{
        font-weight: 700;
        color: white;
        padding: 1em 2em;
        background-color: #0A78B8;
        border-radius: 0.5em;
    }

    p {
        font-weight: 700;
        color: white;
        padding: 1em 2em;
        background-color: #023E8A;
        border-radius: 0.5em;
    }

    img {
        border-radius: 1em;
        width: 100%;
    }
</style>
