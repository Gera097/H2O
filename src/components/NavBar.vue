<template>
    <header>
        <nav class="wrapper">
            <h1>H2O MÉXICO</h1>
            <div>
                <RouterLink class="link" to="/">Home</RouterLink>
                <RouterLink class="link" to="/about">Animals</RouterLink>
                <RouterLink class="link" to="/about">Community</RouterLink>
                <RouterLink class="link" to="/about">Join</RouterLink>
            </div>
        </nav>
    </header>
    <RouterView />
 </template>

<style scoped>
    .wrapper {
        display:flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
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
</style>