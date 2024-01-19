<template>
  <h1>Hola Mundo</h1>
</template>
<script setup lang="ts">
import axios from 'axios'
import { ref, onMounted } from 'vue'

   const app = ref()
   info: []

  onMounted(() => {
    axios
    .get('https://pokeapi.co/api/v2/pokemon/squirtle')
    .then(response => {this.info = response.data.pokemon })
    console.log(response);
  })



</script>
