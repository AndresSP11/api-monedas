<script setup>
  import {ref} from 'vue'
  const monedas = ref([
      { codigo: 'USD', texto: 'Dolar de Estados Unidos'},
      { codigo: 'MXN', texto: 'Peso Mexicano'},
      { codigo: 'EUR', texto: 'Euro'},
      { codigo: 'GBP', texto: 'Libra Esterlina'},
      { codigo: 'PEN', texto: 'Sol Peruano'}
  ])
</script>

<template>
  <div class="contenedor">
    <h1 class="titulo">Cotizador de <span>Criptomonedas</span></h1>
  </div>
  <div class="contenido">
    <form class="formulario">
      <div class="campo">
        <label for="moneda">Moneda:</label>
        <select id="moneda">
          <option value="">--Seleccione--</option>
          <option  v-for="moneda in monedas"
          :value="moneda.codigo"
          >{{ moneda.texto }}</option>
        </select>
      </div>
    </form>
  </div>
</template>

<style scoped>

</style>
