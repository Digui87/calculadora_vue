<script setup>
import Calculadora from './components/Calculadora.vue';
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