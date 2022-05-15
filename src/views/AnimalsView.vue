<script setup>
import AnimalGrid from "@/components/AnimalGrid.vue";
import AnimalFinder from "@/components/AnimalFinder.vue";
</script>
<template>
    <div class="container">
        <AnimalFinder class="buscador"/>
        <AnimalGrid class="animal-grid"/>
    </div>
    
</template>
<style>
    .container {
        background-color: #02023A;
    }
    .animal-grid{
        padding: 0em 2.5em;
    }
    .buscador {
        padding: 2.5em 0em 0.5em;
    }
</style>
