<template>
    <nav class="navbar">
        <div class="logo">
            <a href="/">
                <img alt="Vue logo" src="./../../assets/logo.png">
            </a>
        </div>

        <div class="links">
            <router-link class="link-item" to="/">Home</router-link>
            <router-link class="link-item" to="/about">About</router-link>
        </div>
    </nav>
</template>

<script>
    export default {
        name: 'NavbarTemplate'
    }
</script>

<style scoped>
    .navbar {
        padding: 5px 0;
    }
    a {
        color: #fff;
        text-decoration: none;
    }

    a img {
        max-width: 80px;
        padding: 10px;
    }

    .logo {
        width: 100%;
    }

    .links {
        width: 100%;
    }

    .links .link-item {
        margin: 0 10px;
    }
</style>