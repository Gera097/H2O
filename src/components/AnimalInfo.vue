<template>
    <div class="card">
        <div class="top">
            <img :src="imgRoute" alt="">
            <div class="animal-descript">
                <h2>{{name}}</h2>
                <p>{{description}}</p>
            </div>
        </div>
        <div class="bottom">
            <ul>
                <li>Endangered Level: {{nivelPeligro}}</li>
                <li>Region: {{region}}</li>
            </ul>
        </div>
    </div>
</template>

<script setup>
    defineProps(["name", "imgRoute","description","nivelPeligro","region"]);
</script>

<style scoped>
    .card {
        margin: auto auto;
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
        grid-template-areas: 
                            "top"
                            "bottom";
        color: #F6F6F6;
        border-radius: 1em;
        width: 70%;
        max-height: 500px;
        background-color: #023E8A;
    }

    img {
        max-height: 150px;
        border-radius: 1em;
    }
    .top {
        grid-area: top;
        display: grid;
        grid-template-columns: 1fr 3fr;
        grid-template-rows: 1fr;
        grid-template-areas: 
                            "left right";
        place-items: center;
    }

    .top img {
        grid-area: left;
    }

    .top h2, .top p {
        grid-area: right;
        padding: 0em 15%;
        text-align: justify;
    }
    .top h2 {
        text-align: center;
        text-decoration: underline;
    }
    .bottom {
        text-align: center;
        grid-area: bottom; 
        margin: 5%;
    }
</style>