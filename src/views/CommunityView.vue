<script setup>
    import ActiveEventCardVue from '../components/ActiveEventCard.vue';
    import UserBannerVue from '../components/UserBanner.vue';
</script>
<template>
    <ActiveEventCardVue img-route="./src/assets/fish_icon.svg" title="BEACH CLEANING" location="Mérida, Yucatán, México." date="6/6/22" n-days=2 n-hours=48 n-points=480000 class="active-event"/>
    <ActiveEventCardVue img-route="./src/assets/water_bottle.svg" title="TRASH RECYCLING" location="Cancún, Quintana Roo, México." date="6/20/22" n-days=1 n-hours=8 n-points=80000 class="active-event"/>
    <UserBannerVue/>
    

</template>
<style scoped>
    .active-event {
        margin: 1em 0px;
        height: fit-content;
    }
</style>