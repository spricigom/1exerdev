<script setup>
import { ref } from 'vue';
const contador = ref (0)
function decrementar(){
  if (contador.value > 0){
    contador.value--
  }
}

function reiniciar(){
  contador.value = 0;
}

</script>

<template>
  <button @click="contador++">Adicionar</button>
  <button @click="decrementar">Subtrair</button>
  <button @click="reiniciar">Reiniciar</button>
  <p>valor do contador : {{ contador }}</p>
</template>

<style scoped>
  button{
    background-color: palevioletred;
    color: black;
    font-weight: bolder;
    border-radius: 2px;
    margin: 3px;
    padding: 20px;
  }
</style>