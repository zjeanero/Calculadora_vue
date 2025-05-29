<script>
  import Cabecalho from './components/Cabecalho.vue'
  import Calculadora from './components/Calculadora.vue'

export default {
  name: 'App',
  components: {
    Cabecalho,
    Calculadora
  }
}
</script>

<template>
  <div id="app">
    <Cabecalho />
    <Calculadora />
  </div>
</template>

<style scoped>
  #app {
    padding: 20px;
    text-align: center;
  }
</style>
