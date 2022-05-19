<script setup>
    import {ref} from 'vue';
    import AnimalInfoVue from "@/components/AnimalInfo.vue";
    import ModalVue from '../components/Modal.vue';
    defineProps(["name", "imgRoute"]);
    
const showModal = ref(false)
</script>

<template>
<Teleport to="body">
    <ModalVue :show="showModal" @close="showModal = false">
        <template #body>
            <AnimalInfoVue name="Mexican Axolotl" img-route="https://www.24-horas.mx/wp-content/uploads/2019/11/ajolote.jpg?w=800" description="With the scientific name Ambystoma mexicanum, it is a creature whose curious appearance earned it the name of water monster (axolotl) among the Nahuatl tribe.
        It is possible to find it in the canals of the city of Xochimilco, but there are fewer and fewer specimens that exist in freedom, so most of them live in aquariums throughout the world." nivelPeligro="Extreme" region="Laguna de Xochimilco"/>
        </template>
    </ModalVue>
</Teleport>
<button class="img-card" @click="showModal = true">
    <img :src="imgRoute" alt="">
    <p>{{name}}</p>
</button>
</template>

<style scoped>
    .img-card {
        border: none;
        background-color: #02023a00;
    }

    .img-card:hover p{
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
