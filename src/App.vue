<script setup>

import { ref, computed } from 'vue';

const numero1 = ref(0);
const numero2 = ref(0);
const operacao = ref('');

const resultado = computed(() => {
    switch (operacao.value) {
        case 'somar':
            return numero1.value + numero2.value;
        case 'diminuir':
            return numero1.value - numero2.value;
        case 'multiplicar':
            return numero1.value * numero2.value;
        case 'dividir':
            return numero1.value / numero2.value;
        default:
            return 0;
    }
})

</script>

<template>
  <div class="container">
    <header class="p-5 mb-5 mt-5 bg-secondary rounded-3">
      <h1>Calculdadora Aritmética</h1>
    </header>
    <div class="row">
      <div class="col-md-5">
        <input type="number" v-model="numero1">
      </div>
      <div class="col-md-2">
        <select v-model="operacao" class="form-control">
          <option value="somar">Somar</option>
          <option value="diminuir">Diminuir</option>
          <option value="multiplicar">Multiplicar</option>
          <option value="dividir">Dividir</option>
        </select>
      </div>
      <div class="col-md-5">
        <input type="number" v-model="numero2">
      </div>
    </div>
    <h2 class="mt-5">Resultado: {{ resultado }}</h2>
  </div>
</template>

<style scoped>
.container {
  max-width: 640px;
  text-align: center;
}
</style>