<script setup>
defineProps({
  msg: {
    type: String
  },
});
</script>

<template>
    <button>
        {{msg}}
    </button>
</template>

<style scoped>
    button {
        width:fit-content;
        padding: 0.5em 1em;
        background-color: #023E8A;
        color: white;
    }
</style>

