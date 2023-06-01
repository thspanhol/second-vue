<template>
    <h1 v-if="trabalhando">Trabalho com os Seguintes Frameworks:</h1>
    <h1 v-else>Estudo os seguintes Frameworks:</h1>
    <h3>{{ primeiro }}</h3>
    <h3>{{ segundo }}</h3>
  </template>
  
  <script>
  export default {
    name: 'InfoFrameworks',
    data() {
      return {
        primeiro: 'React',
        segundo: 'Vue',
        trabalhando: false,
      }
    }
  }
  </script>