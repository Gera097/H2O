<template>
<div class="slider-container">  
  <img
    class="slider-item"
    src="@/assets/VaquitaMatina.png"
  />
  <img
    class="slider-item"
    src="@/assets/Guacamaya.png"
  />
  <img
    class="slider-item"
    src="@/assets/Jaguar.png"
  />
</div>
</template>

<style>
   .slider-container {
  display: flex;
  width: 100%;
  overflow-x: scroll;

  scroll-snap-type: x mandatory;
}

.slider-container img {
  flex: 0 0 100%;
  width: 100%;
  border-radius: 10px;
  border: 10px;
  background-color:#0095c79a;
  object-fit:contain;
  

  scroll-snap-align: center;
}
/* Works on Firefox */
* {
  scrollbar-width: thin;
  scrollbar-color: #02023A orange;
}

/* Works on Chrome, Edge, and Safari */
*::-webkit-scrollbar {
  width: 12px;
}

*::-webkit-scrollbar-track {
  background: 02023A;
}

*::-webkit-scrollbar-thumb {
  background-color:#0096C7;
  border-radius: 20px;
  border: 3px solid #02023A;
}
</style>

<script setup>
</script>