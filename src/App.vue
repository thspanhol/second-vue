<template>
  <h1>Olá Mundo!</h1>
  <PrimeiroComponente />
  <LifeCycle />
  <UsaProps recebeProps="Usei Props direta" />
  <UsaProps :recebeProps="PropsData" />
  <h1>{{ counter }}</h1>
  <AlteraContador @aumentar-contador="aumentarContador" />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import UsaProps from './components/UsaProps.vue'
import AlteraContador from './components/AlteraContador.vue'

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    UsaProps,
    AlteraContador
  },
  data() {
    return {
      PropsData: 'Passei o data como Props',
      counter: 0
    }
  },
  methods: {
    aumentarContador() {
      this.counter = this.counter +1
    }
  }
}
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}
a {
  color: plum;
}
</style>
