<script setup>
import { ref, computed } from 'vue'

const cidadesLista = ref(['São Paulo',
  'Rio de Janeiro',
  'Belo Horizonte',
  'Salvador',
  'Fortaleza',
  'Curitiba',
  'Manaus',
  'Recife',
  'Porto Alegre',
  'Brasília',
])


const novaCidade = ref('')

function adicionar() {
  cidadesLista.value.push(novaCidade.value)
  novaCidade.value = ''
}

function remover(index) {
  cidadesLista.value.splice(index, 1)
}
const cidadesOrdenadas = computed(() => {
  return cidadesLista.value.sort();
})
</script>

<template>
 <button @click="remover(index)">Remover</button>
  <input type="text" v-model="novaCidade">
  <button @click="adicionar">Adicionar</button>
  <ul>
    <li v-for="(cidade, index) in cidadesOrdenadas" :key="index">{{ cidade }}</li>
  </ul>
</template>
