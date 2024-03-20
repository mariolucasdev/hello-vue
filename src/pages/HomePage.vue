<script setup>
import { ref } from 'vue'
import NavbarTemplate from './../components/Template/Navbar.vue'

const listItems = ['Item 1', 'Item 2', 'Item 3', 'Item 4', 'Item 5']
const message = ref('My First Component')
const content = ref('This is a simple component vue.')
const textButton = ref('Show Content')
const showContent = ref(false)

const listItem = ref(listItems.map((item, index) => {
    return {
        id: index,
        name: item
    }
}))

const toggleContent = () => {
    showContent.value = !showContent.value
    textButton.value = showContent.value ? 'Hide Content' : 'Show Content'
}

const changeTitle = (event) => {
    message.value = event.target.value
}
</script>

<template>
    <div>
        <div class="main">
            <NavbarTemplate />

            <h1 v-show="showContent">{{ message }}</h1>
            <p v-show="showContent">{{ content }}</p>

            <button v-on:click="toggleContent" v-text="textButton"></button>

            <ul v-show="showContent">
                <li v-for="item in listItem" :key="item.id">{{ item.name }}</li>
            </ul>

            <input v-on:keyup="changeTitle" v-model="message" paceholder="Alterar título">
        </div>
    </div>
</template>

<style scoped>
h1 {
    font-size: 40px;
    margin: 40px 0 0;
}
p {
    font-size: 24px;
    color: #42b983;
}

ul {
    list-style: none;
    padding: 0;
    margin: 0;
}

ul li {
    font-size: 20px;
    margin: 10px 0;
}

input {
    width: 100%;
    padding: 10px;
    margin: 20px 0;
    font-size: 20px;
}
</style>