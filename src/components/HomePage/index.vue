<template>
    <div>
        <div class="main">
            <NavbarTemplate />
            <h1>{{ message }}</h1>
            <p>
            This is a simple component vue.
            </p>
        </div>
    </div>
</template>

<script>
import NavbarTemplate from './../Template/Navbar.vue'

export default {
    name: 'HomePage',
    props: {
        message: String
    },
    components: {
        NavbarTemplate
    }
}
</script>

<style scoped>
h1 {
    font-size: 40px;
    margin: 40px 0 0;
}
p {
    font-size: 24px;
    color: #42b983;
}
</style>