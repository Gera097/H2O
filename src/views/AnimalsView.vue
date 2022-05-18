<script setup>
import AnimalGrid from "@/components/AnimalGrid.vue";
import AnimalFinder from "@/components/AnimalFinder.vue";
import AnimalInfo from "@/components/AnimalInfo.vue";

</script>
<template>
    <div class="container">
            <AnimalFinder class="buscador"/>
            <AnimalInfo name="Mexican Axolotl" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800" description="With the scientific name Ambystoma mexicanum, it is a creature whose curious appearance earned it the name of water monster (axolotl) among the Nahuatl tribe.
            It is possible to find it in the canals of the city of Xochimilco, but there are fewer and fewer specimens that exist in freedom, so most of them live in aquariums throughout the world." nivelPeligro="Extremo" region="Laguna de Xochimilco"/>
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
