<template>
  <div>
    <h2>Contador: {{ contador }}</h2>
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar" :disabled="contador === 0">Decrementar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contador: 0,
    };
  },
  methods: {
    incrementar() {
      this.contador++;
    },
    decrementar() {
      if (this.contador > 0) {
        this.contador--;
      }
    },
  },
};
</script>