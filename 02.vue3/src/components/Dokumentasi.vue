<template>
    <h2>Welcome</h2>
    <h1>{{ nama }}</h1>
    <button @click="changeName">Change Name</button>
    <!-- memanggil link -->
    <a :href="url">Go Web</a>
    <!-- two way data binding -->
    <input type="text" v-model="name" />
    {{ name }}
    <!-- conditional looping -->
    <div v-if="product.length">
        <ul>
            <li v-for="item in product" :key="item.id">
                {{ item.title }} - {{ item.price }}
            </li>
        </ul>
    </div>
    
    <div v-else>
        <p>No Data Found</p>
    </div>
    <!-- input dengan computed properti -->
    <input type="text" v-model="cari" Placeholder="Cari">
    <ul>
        <li v-for="item in cariData" :key="item.id">
            {{ item.title }} - {{ item.price }}
        </li>
    </ul>

    <Header :text="text" />
</template>

<script>
import Header from '@/components/Header.vue'

export default {
    name: 'App',
    data() {
        return {
            nama: "Edward Kristian Mangare",
            // data binding
            url: "https://nihonuwu.com",
            // two way data binding
            name: "",
            // conditional looping
            nama: "",
            product: [
                { id: 1, title: "product 1", price: 3000 },
                { id: 2, title: "product 2", price: 3000 },
                { id: 3, title: "product 3", price: 4000 },
                { id: 4, title: "product 3", price: 6000 },
            ]

        }
    },
    methods: {
        changeName: function () {
            this.nama = "Heru"
        }
    },

    // lifecycle hook
    beforeMount() {
        console.log('Before Mount')
    },
    mounted() {
        console.log('Mounted')
    },
    beforeCreate() {
        console.log('Before Create')
    },
    created() {
        console.log('Created')
    },
    // created() {
    //     this.product = [
    //         { id: 1, title: "product 1", price: 3000 },
    //         { id: 2, title: "product 2", price: 3000 },
    //         { id: 3, title: "product 3", price: 4000 },
    //         { id: 4, title: "product 3", price: 6000 },
    //     ]
    // },

    data() {
        return {
            nama: "",
            product: [],
            cari: "",
        }
    },
    // lifecycle hook
    // beforeMount() {
    //   console.log('Before Mount')
    // },
    // mounted() {
    //   console.log('Mounted')
    // },
    // beforeCreate() {
    //   console.log('Before Create')
    // },
    created() {
        this.product = [
            { id: 1, title: "product 1", price: 3000 },
            { id: 2, title: "product 2", price: 3000 },
            { id: 3, title: "product 3", price: 4000 },
            { id: 4, title: "product 3", price: 6000 },
        ]
    },
    // compoted properti
    computed: {
        cariData() {
            return this.product.filter((item) => {
                return item.title.match(this.cari);
            });
            //fillter function dari javascript
            // match function dari javascript 
        }
    },
    // component
    components: {
        Header
    },
    // props (kirim component induk ke anak)
    data() {
        return {
            text: "ini data"
        }
    },
    // event (kirim component anak ke induk)
    
    methods: {
        changeText() {
            this.$emit("changeTitle", this.newText)
        }
    },
    // mendaftarkan emits
    emits: ["changeTitle"],

    // untuk vue
    data() {
        return {
            text: "ini data"
        }
    },
    methods: {
        ubahText(newText) {
            this.text = newText;
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
