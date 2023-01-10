<!-- <template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Selamat Datang Di Dalam Aplication Website"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
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
</style> -->

<template>
  <div id="app">
    <div class="container">
      <h1 class="mb-4">Daftar Pelanggan</h1>
      <customer-table />
    </div>
  </div>
</template>

<script>
import CustomerTable from '@/components/CustomerTable.vue'

export default {
  name: 'App',
  components: {
    CustomerTable
  },
  // data() {
  //   return {
  //     customers: [
  //       {
  //         id: 1,
  //         name: 'Bambang',
  //         email: 'bambang@mail.com',
  //         address: 'Jl.Kenanga',
  //       },
  //       {
  //         id: 2,
  //         name: 'Dika',
  //         email: 'dika@mail.com',
  //         address: 'Jl.Mangga',
  //       },
  //       {
  //         id: 3,
  //         name: 'Agus',
  //         email: 'agus@mail.com',
  //         address: 'Jl.Mataram',
  //       },
  //     ],
  //   }
  // },
  data() {
    return {
      items: [{ message: 'Foo' }, { message: 'Bar' }]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>