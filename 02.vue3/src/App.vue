<template>
  <div v-if="product.length">
  <ul>
    <li v-for="item in product" :key="item.id">
      {{ item.title }} - {{  item.price }}
    </li>
  </ul>
  </div>
  
  <div v-else>
    <p>No Data Found</p>
  </div>
  
</template>

<script>

export default {
  name: 'App',
  data () {
    return {
      nama: "",
      product:[
        {id: 1, title: "product 1", price:3000},
        {id: 2, title: "product 2", price:3000},
        {id: 3, title: "product 3", price:4000},
      ]
    }
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
</style>
