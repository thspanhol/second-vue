<template>
  <h1 v-if="trabalhando">Trabalho com os Seguintes Frameworks:</h1>
  <h1 v-else>Estudo os seguintes Frameworks:</h1>
  <h3>{{ primeiro }}</h3>
  <h3>{{ segundo }}</h3>
  <h2><a v-bind:href="meu_link" target="_blank">Meu GitHub</a></h2>
  <button @click="showEmail">{{ texto_email }}</button>
  <h2 v-show="mostrar_email">{{ email }}</h2>
</template>

<script>
export default {
  name: 'InfoFrameworks',
  data() {
    return {
      primeiro: 'React',
      segundo: 'Vue',
      trabalhando: true,
      meu_link: 'https://github.com/thspanhol',
      email: 'thales_spanhol@hotmail.com',
      mostrar_email: false,
      texto_email: 'Mostrar Email'
    }
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email
      this.texto_email === 'Mostrar Email'
        ? (this.texto_email = 'Esconder Email')
        : (this.texto_email = 'Mostrar Email')
    }
  }
}
</script>

<style scoped>
  a {
    color: brown;
  }
</style>