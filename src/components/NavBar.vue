<template>
    <header>
        <nav class="wrapper">
            <img src="@/assets/logo_h2o.png" alt="Logo H2O">
            <div>
                <RouterLink class="link" to="/">Home</RouterLink>
                <RouterLink class="link" to="/animals">Animals</RouterLink>
                <RouterLink class="link" to="/animals">Community</RouterLink>
                <RouterLink class="link" to="/animals">Join</RouterLink>
            </div>
        </nav>
    </header>
    <RouterView />
 </template>

<style scoped>
    .wrapper {
        display:flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 0 3em;
    }

    .link {
        margin: 0.5em;
        text-decoration: none;
    }
    nav {
        background-color: #03045E;
        height: 5em;
    }
    h1 {
        color: white;
    }
    a {
        font-size: medium;
        color: white;
    }

    img {
        max-height: 3em;
    }
</style>