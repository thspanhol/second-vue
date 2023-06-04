<template>
  <div>
    <h1>Meu nome é: {{ nome }}</h1>
    <InfoFrameworks />
  </div>
</template>

<script>
import InfoFrameworks from './InfoFrameworks.vue'

export default {
  name: 'LifeCycle',
  data() {
    return {
      nome: 'Ainda não sei'
    }
  },
  created() {
    setTimeout(() => {
      this.nome = 'Thales'
    }, 1000)
  },
  mounted() {
    setTimeout(() => {
      this.nome = 'Spanhol'
    }, 2000)
  },
  components: {
    InfoFrameworks
  }
}
</script>
