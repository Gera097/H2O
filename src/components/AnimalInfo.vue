<template>
    <div class="card">
        <div class="top">
            <div class="image">
                <img :src="imgRoute" alt="">
            </div>
            <div class="animal-descript">
                <h2>{{name}}</h2>
                <p>{{description}}</p>
            </div>
        </div>
        <div class="bottom">
            <div id="mapa-ubi">

            </div>
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
        grid-template-areas: 
                            "top"
                            "bottom";
        color: #F6F6F6;
        border-radius: 1em;
        max-width: 90%;
        min-width: 300px;
        background-color: #023E8A;
        justify-content: center;
        padding: 1em;
    }

    .top {
        grid-area: top;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }
    .image {
        padding: 1em;
        max-width: 40%;
        min-width: 350px;
        align-items: center;
        place-self: center;
        border-radius: 1em;
        
    }
    img {
        width: 100%; 
        border-radius: 1em;
    }

    .animal-descript {
        max-width: 50%;
        min-width: 350px;
    }
    .top h2, .top p {
        padding: 0em 15%;
        text-align: justify;
    }
    .top h2 {
        text-align: center;
        text-decoration: underline;
    }
    .bottom {
        grid-area: bottom; 
        display: flex;
        flex-wrap: wrap;
        text-align: center;
        justify-content: center;
        align-items: center;
    }
    #mapa-ubi {
        flex:1 1 35%;
        aspect-ratio: 16 / 9;
        background-color: aliceblue;
        border-radius: 1em;
    }
    ul {
        padding: 0%;
        min-width: 40%;
        max-width: 50%;
        list-style: none;
    }

    @media screen and (max-width: 860px) {
        .bottom {
            grid-area: bottom; 
            display: flex;
            flex-wrap: wrap;
            text-align: center;
            justify-content: center;
            align-items: center;
        }
        #mapa-ubi {
        flex:1 1 50%;
        aspect-ratio: 16 / 9;
        background-color: aliceblue;
        border-radius: 1em;
        margin: 5% 10%;
        }
        .animal-descript {
        max-width: 100%;
        min-width: 350px;
        }
    }
</style>