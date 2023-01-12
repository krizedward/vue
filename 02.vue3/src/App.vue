<template>
  <!-- custom events -->
  <Header @changeTitle="ubahText" :text="text" />  
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'App',
  // components header
  components: {
    Header
  },
  // Custom Event
  data () {
    return {
      text: "ini data"
    }
  },
  methods: {
    ubahText(newText){
      this.text = newText;
    }
  },
  // vue router
  // merender disisi client
  
};
</script>

<style>
</style>
