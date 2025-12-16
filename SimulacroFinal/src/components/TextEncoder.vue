<template>
  <div>
    <textarea v-model="inputText" placeholder="Ingresa tu texto aquí"></textarea>
    <button @click="encodeText">Codificar</button>
    <p>Resultado: {{ encodedText }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
    };
  },
  computed: {
    encodedText() {
      return this.encode(this.inputText).toUpperCase();
    },
  },
  methods: {
    encode(text) {
      text = text.toLowerCase();
      return text
        .replace(/a/g, 'u')
        .replace(/e/g, 'o')
        .replace(/o/g, 'e')
        .replace(/u/g, 'a');
    },
    encodeText() {
      // Método para codificar si se requiere otras acciones al hacer clic
    },
  },
};
</script>