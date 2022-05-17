<script setup>
import VueButton from "@/components/Button.vue";
import Carrusel from "@/components/Carrusel.vue";
</script>

<template>
  <main>
    <div class="portrait-container">
    <img src="@/assets/home_portrait.png" alt="Persona cortando basura atorada en su lancha, en el mar">
    <h2 class="portrait-text">DISCOVER HOW YOU CAN <span>HELP OUR OCEANS</span></h2>
    </div>
    <h2>BE PART OF OUR <span class="enfasis">COMUNNITY</span></h2>
    <img class="mapa-comunidades" src="@/assets/mapa_mexico.png" alt="Comunidades de H2O en México">
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
    <VueButton class="join-button" msg="JOIN NOW"/>
    <div class="carroussel-container">
      <Carrusel class="carrusel"/>
      <div class="right-container">
        <h3>LEARN HOW TO HELP <span>ENDANGERED SPECIES</span></h3>
        <VueButton msg="DISCOVER MORE" class="discover-button"/>
      </div>
      
    </div>
  </main>
</template>

<style scoped>

  main {
    min-width: 350px;
    display: grid;
    justify-content: center;
    gap: 1em;
  }

  .portrait-container {
    position: relative;
    height: fit-content;
    width: 100%;
  }


  .portrait-text {
    font-size: 3vw;
    position: absolute;
    top: 10%;
    left: 8%;
    width: 25%;
    text-align: center;
    z-index: 1;
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
    font-size: calc(1em + 2vw);
    justify-self: center;
    text-align: center;
  }
  span {
    color: #13abf1;
  }
  .enfasis {
    text-decoration: underline;
  }

  .card {
    max-width: 250px;
    text-align: center;
  }

  img {
    width: 100%;
    height: auto;
  }
  .mapa-comunidades {
    place-self: center;
    width:90%;
  }
  .svg-icon {
    width: auto;
    height: 102.12px; 
  }

  .join-button {
    place-self: center;
    border-color: #F6F6F6;
    border-radius: 0.3em;
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

  .discover-button {
    background-color: #023E8A;
    box-shadow: -13px 14px 4px rgba(0, 0, 0, 0.15);
    font-weight: 700;
    border-radius: 7px;
    border-color: rgba(0, 0, 0, 0.15);
  }

  .right-container {
    font-size: 2em;
    place-self: center;
    text-align: center;
  }


</style>