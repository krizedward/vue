<template>
    <h2>{{ text }}</h2>
    <button @click="changeText">Ubah Text</button>
</template>

<script>
    export default {
        name:"app-header",
        // props
        props: ["text"],
        data () {
            return {
                newText : "ini adalah text dari header.vue"
            }
        },
        methods: {
            changeText() {
                this.$emit("changeTitle", this.newText)
            }
        },
        // mendaftarkan emits
        emits: ["changeTitle"]
    }
</script>

<style></style>