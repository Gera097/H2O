<script setup>
import AnimalCard from "@/components/AnimalCard.vue";
</script>
<template>
    <div class="grid-container">
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
        <AnimalCard name="Ajolote mexicano" img-route="/src/assets/Ajolote.png"/>
    </div>
    
</template>
<style scoped>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
        grid-template-columns: repeat(auto-fill, minmax(min(280px, 50%), 1fr)); 
    }
</style>
