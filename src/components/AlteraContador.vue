<template>
  <div>
    <button @click="$emit('aumentarContador')">+1</button>
  </div>
</template>

<script>
export default {
  name: 'AlteraContador',
  emits: ['aumentarContador']
}
</script>
