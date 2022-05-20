<script setup>
    const props = defineProps({
        imgRoute: String,
        title: String,
        location: String,
        date: String,
        nDays: String,
        nHours: String,
        nPoints: String 
    })
</script>
<template>
    <div class="event-card">
        <div class="left-container">
            <div class="event-img-container">
                <img :src=imgRoute alt="">
            </div>  
            <div class="event-info">
                <h3>{{title}}</h3>
                <p class="location">{{location}}</p>
                <p class="duration">{{nDays}} days/ {{nHours}}hrs/ {{nPoints}}pts</p>
            </div> 
        </div>
        <p class="date">{{date}}</p>
    </div>
</template>
<style scoped>
    .event-card {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #FFFFFF;
        box-shadow: 0px 0px 20px 4px rgba(0, 0, 0, 0.25);
        border-radius: 10px;
    }
    .left-container{
        display: flex;
        align-items: center;
        gap: 0.5em;
    }
    .event-img-container {
        background-color: rgba(3, 4, 94, 1);
        border-radius: 0.5em;
        margin: 5px 5px;
    }
    .event-img-container img {
        display: block;
        margin: 30% auto;
        width: 75%;
    }
    h3, p {
        margin: 0em;
    }
    h3 {
        margin-bottom: 0.25em;
        font-weight: 700;
        color: rgba(10, 120, 184, 1);
    }

    .location {
        margin-bottom: 0.25em;
        font-weight: 500;
        color: #03045E;
        font-size: 1em;
    }
    .duration{
        font-weight: 500;
        color: #03045E;
        font-size: 0.75em;
    }
    .date {
        font-size: 1.25em;
        font-weight: 700;
        letter-spacing: 0em;
        text-align: center;
        color: #E7B840;
        margin-right: 1em;
    }
</style>