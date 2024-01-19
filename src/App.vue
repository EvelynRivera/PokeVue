<template>
  <h1>Hola Mundo</h1>
  <div>
    {{ squirtle }}
  </div>
</template>
<script setup lang="ts">
import axios from 'axios';
import { ref, onMounted } from 'vue';

// Propiedades reactivas
const squirtle = ref<any>();

// Propiedades computadas

// Métodos
const getData = () => {
  axios.get('https://pokeapi.co/api/v2/pokemon/squirtle').then((res) => {
    squirtle.value = res.data;
  });
};

// Hooks (Métodos del ciclo de vida Vue)
onMounted(() => {
  getData();
});
</script>
