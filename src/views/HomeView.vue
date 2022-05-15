<script setup>
import TheWelcome from "@/components/TheWelcome.vue";
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
</style>