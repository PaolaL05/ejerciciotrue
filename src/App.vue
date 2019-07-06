<template>
  <div id="app">
    <button @click="actRep"> Repositorios </button>
    <HelloWorld v-if="activeBool" msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  data() {
    return{
    activeBool:false
    }
  },
  components: {
    HelloWorld
  },
  methods: {
    actRep(){      
      this.activeBool = !this.activeBool
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
