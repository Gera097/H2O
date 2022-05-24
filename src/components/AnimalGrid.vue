<script setup>
import AnimalCard from "@/components/AnimalCard.vue";
import axios from "axios";
import { onMounted, ref } from "vue";
let data = ref([])
function getData(path) {
    axios.get(path).then(response => {
        console.log(response.data);
        data.value = response.data;
    })
}
onMounted(() => {
    getData("./src/mock/animal_photo.json");
    console.log(`la siguiente es la data: ${data}`);
})

</script>
<template>
    <div v-if="data" class="grid-container">
        <AnimalCard v-for="animal in data" :name="animal.name" :img-route="animal.photo_link" />
    </div>
    
</template>
<style scoped>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); 
        gap: 1em;
        margin: 2em 2em 0px 2em;
    }
</style>
