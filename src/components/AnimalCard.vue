<script setup>
    import {ref} from 'vue';
    import AnimalInfoVue from "@/components/AnimalInfo.vue";
    import ModalVue from '../components/Modal.vue';
    import CRUD from '../lib/utils/crud.js'
    const props = defineProps(["name", "imgRoute"]);
    let info = ref(null);
    let showModal = ref(false);
    
    async function clic_event (){
        showModal.value = true;
        let response = await CRUD.get("./src/mock/"+props.name+".json");
        info.value = response.data;
        console.log(info.value)   
    } 
</script>

<template>
<Teleport to="body">
    <ModalVue :show="showModal" @close="showModal = false">
        <template v-if="info" #body>
            <AnimalInfoVue :name="info.name" :img-route="info.link" :description="info.description" :nivelPeligro="info.level" :region="info.region"/>
        </template>
    </ModalVue>
</Teleport>
<button class="img-card" @click="clic_event">
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
        height: 200px;
    }
</style>
