<script setup>
import VueButton from "@/components/Button.vue";
import Carrusel from "@/components/Carrusel.vue";
</script>

<template>
  <main>
    <img src="@/assets/home_portrait.png" alt="Persona cortando basura atorada en su lancha, en el mar">
    <h2>BE PART OF OUR <span class="enfasis">COMUNNITY</span></h2>
    <img src="@/assets/mapa_mexico.png" alt="">
    <div class="horizontal-list">
      <div class="card">
        <h3>JOIN LOCAL EVENTS</h3>
        <img class="svg-icon" src="@/assets/saludo_mano.svg" alt="">
      </div>
      <div class="card">
        <h3>WIN PRIZES BY SAVING OUR OCEANS</h3>
        <img class="svg-icon" src="@/assets/galardon.svg" alt="">
      </div>
      <div class="card">
        <h3>SHARE ON YOUR SOCIAL MEDIA</h3>
        <img class="svg-icon" src="@/assets/hashtag.svg" alt="">
      </div>
    </div>
    <VueButton class="center" msg="JOIN NOW"/>
    <div class="carroussel-container">
      <Carrusel class="carrusel"/>
      <div class="right-container">
        <h3>LEARN HOW TO HELP ENDANGERED SPECIES</h3>
      </div>
      
    </div>
  </main>
</template>

<style scoped>

  main {
    display: grid;
  }

  .horizontal-list {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }
  h2, h3 {
    color: #03045E;
  }
  h2 {
    justify-self: center;
  }
  .enfasis {
    text-decoration: underline;
    color: #6ad0ff;
  }

  .card {
    max-width: 250px;
    text-align: center;
  }

  img {
    width: 100%;
    height: auto;
  }
  .svg-icon {
    width: auto;
    height: 102.12px; 
  }

  .center {
    place-self: center;
    margin: 3em;
  }
  .carroussel-container {
    display: grid;
    grid-template-columns: 50% 50%;
    grid-template-rows: 1fr 75% 1fr;
    grid-template-areas: 
      ". ."
      "left right"
      ". .";
    background-color: #02023A;
  }

  .carroussel-container h3{
    color: white;
  }
  .carrusel {
    grid-area: left;
    justify-self: center;
  }

  .right-container {
    grid-area: right;
  }

</style>