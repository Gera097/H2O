<script setup>
</script>
<template>
<div class="user-banner">
    <div class="content">
        <img class="profile-picture" src="./../assets/Ajolote.png" alt="user profile picture">
        <h2>Gerardo Sánchez</h2>
        <div class="score">
            <p>POINTS IN THIS MONTH</p>
            <p class="number">172,000</p>
            <p>TOTAL EVENTS PARTICIPATED</p>
            <p class="number">17</p>
            <p>TOTAL EVENTS ORGANIZED</p>
            <p class="number">3</p>
        </div>

        <div class="contact">
            <p>EMAIL</p>
            <p class="personal-info">g.sanchezalba@outlook.com</p>
            <p>PHONE NUMBER</p>
            <p class="personal-info">4641881555</p>
            <p>REGION</p>
            <p class="personal-info">GUANAJUATO</p>
        </div>
    </div>
</div>
</template>
<style scoped>
 .user-banner {
     display: grid;
     grid-template-columns: 5% auto 5%;
     width: fit-content;
     height: fit-content;
     background-color: #0A78B8;
     border-radius: 0 0 25% 0;
     align-items: center;
     padding: 3% 0 5%;
 }
 .content {
     grid-column: 2 / -2;
     display: flex;
     flex-direction: column;
     align-items: center;
 }
 .profile-picture {
     display: block;
     border-radius: 50%;
     width: 50%;
 }
.score, .content {
    text-align: center;
}
 p,h2 {
     color: white;
 }

 p {
     font-weight: 700;
     font-style: italic;
 }
 .personal-info {
     font-weight: 500;
 }
 .number {
     font-size: xx-large;
 }
</style>