<template>
  <div id="app">
<!--    <img alt="Vue logo" src="./assets/logo.png">-->
<!--    <HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <configurator></configurator>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Configurator from "@/components/Configurator";

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Configurator
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

    #app {
        font-family: toyotadisplay_bd,Arial,Helvetica,sans-serif;;
    }

   header h1 {
        display: inline-block;
    }
</style>
