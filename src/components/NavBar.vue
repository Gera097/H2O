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
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: center;
        padding: 0px 5em;
        gap: 0px 20px;
    }
    @media (max-width: 700px) {
        .wrapper {
        display:flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        padding: 0%;
        gap: 0px 20px;
    }
    } 
    .link {
        margin: 0.5em;
        text-decoration: none;
    }
    nav {
        background-color: #03045E;
        height:5rem;
        min-width: 350px;
    }
    h1 {
        color: white;
    }
    a {
        font-weight: 500;
        color: white;
    }
    a:hover {
        font-weight: 700;
        color: white;
    }

    img {
        max-height: 3em;
    }
</style>