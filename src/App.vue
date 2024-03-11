<script setup>
import {ref} from 'vue'

const listaCidades = ['São Paulo',
  'Rio de Janeiro',
  'Belo Horizonte',
  'Salvador',
  'Fortaleza',
  'Curitiba', 
  'Manaus', 
  'Recife', 
  'Porto Alegre',
  'Brasília',]
</script>

<template>
  <ul>
    <li v-for="(listaCidades, index) in listaCidades" :key="index"> {{ listaCidades }}</li>
  </ul>
</template>
