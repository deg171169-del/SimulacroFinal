<template>
  <div id="app">
    <h1>Codificador de Texto</h1>
    <TextEncoder />
    <p>respuestas: 1-b, 2-b, 3-c, ...</p>
  </div>
</template>

<script>
import TextEncoder from './components/TextEncoder.vue';

export default {
  components: {
    TextEncoder,
  },
};
</script>