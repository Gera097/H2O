<script setup>
import AnimalCard from "@/components/AnimalCard.vue";
</script>
<template>
    <div class="grid-container">
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
        <AnimalCard name="Ajolote mexicano" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800"/>
    </div>
    
</template>
<style scoped>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); 
        justify-items: center;
        gap: 1em;
        margin: 2em 2em 0px 2em;
    }
</style>
