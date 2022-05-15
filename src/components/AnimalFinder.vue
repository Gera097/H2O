<template>
    <div class="search-container">
        <h1>KNOW THE <span>ANIMAL</span></h1>
        <div class="search">
            <form action="#">
                <input type="text"
                    placeholder="Ajolote Mexicano"
                    name="search">
                <button>
                    Search
                </button>
            </form>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>

    form {
        display: flex;
        justify-content: center;
    }
    .search-container {
        display: block;
        margin-left: auto;
        margin-right: auto;
        text-align: center;
    }
    input {
        width: 40%;
        border: none;
        padding: 1em 2em 0.5em;
        border-radius: 1em 0px 0px 1em;
    }
    button {
        width: 10%;
        margin-left: 0.5%;
        border: none;
        font-weight: 600;
        background-color: #08a860;
        color: white;
        padding: 0.5em;
        border-radius: 0px 1em 1em 0px;
    }
    button:hover {
        width: 10%;
        margin-left: 0.5%;
        border: none;
        font-weight: 600;
        background-color: #63C196;
        color: white;
        padding: 0.5em;
        border-radius: 0px 1em 1em 0px;
    }
    h1 {
        margin: 0px;
        color: white;
    }
    span {
        color: #5cb8ee;
    }
</style>