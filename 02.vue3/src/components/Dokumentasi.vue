<template>
    <h2>Welcome</h2>
    <h1>{{ nama }}</h1>
    <button @click="changeName">Change Name</button>
    <!-- memanggil link -->
    <a :href="url">Go Web</a>
    <!-- two way data binding -->
    <input type="text" v-model="name" />
    {{ name }}
</template>

<script>

export default {
    name: 'App',
    data() {
        return {
            nama: "Edward Kristian Mangare",
            // data binding
            url: "https://nihonuwu.com",
            // two way data binding
            name: "",

        }
    },
    methods: {
        changeName: function () {
            this.nama = "Heru"
        }
    },
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
