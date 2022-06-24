<template>
  <div id="app">
    <Usuarios_tabla/>
  </div>
</template>

<script>
import Usuarios_tabla from './components/Usuarios_tabla.vue'

export default {
  name: 'App',
  components: {
    Usuarios_tabla
  }
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 30px;
  margin-left: 350px;
}
</style>
