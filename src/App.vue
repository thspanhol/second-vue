<template>
  <h1>Olá Mundo!</h1>
  <PrimeiroComponente />
  <LifeCycle />
  <UsaProps recebeProps="Usei Props direta" />
  <UsaProps :recebeProps="PropsData" />
</template>

<script>
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import UsaProps from './components/UsaProps.vue';

export default {
  name: 'App',
  components: {
    PrimeiroComponente,
    LifeCycle,
    UsaProps,
  },
  data() {
    return {
      PropsData: 'Passei o data como Props',
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
