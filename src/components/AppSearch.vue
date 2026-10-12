<script setup>
import { ref } from 'vue'

defineProps({
  titulo: String
})

const emit = defineEmits(['buscar'])
const texto = ref('')

function buscar() {
  emit('buscar', texto.value)
}

function limpar() {
  texto.value = ''
  emit('buscar', '')
}
</script>

<template>
  <div class="campo">
    <img class="iconesearch" src="/search.svg" @click="buscar">
    <input
      v-model="texto"
      placeholder="Procure seu modelo 3D..."
      class="inputsearch"
      @keyup.enter="buscar"
    >
    <img class="iconeclose" src="/close.svg" @click="limpar">
  </div>
</template>

<style scoped>
.campo {
  position: sticky;
  top: 0;
  top: 10px;
  left:0px;
  right:0px;
  z-index: 1000;
  background-color: white;
  margin:9px;
  padding: 5px;
  gap: 5px;
  min-width:0;
  display: flex;
  justify-content: space-between;
  border-style: solid;
  border-color: black
}

.inputsearch {
  flex: 2;
  border-style: none;
  height: 30px;
  font-size:1.15rem;
  background-color:white;
  outline: none;
  min-width:0;
  color: black;
} 

.div h1 {
  margin: 0;
  font-size: 1.5rem;
}

.div p {
  margin-bottom: 0;
}
.iconesearch{
  width: 100%;
  max-width: 35px; 
  flex: 1;
  flex-shrink:0;
}
.iconeclose{
  width: 100%;
  max-width: 35px;
  flex: 1;
  flex-shrink:0;
  transition: all 0.3s ease;
}
.iconeclose:hover{
  filter: brightness(0) saturate(100%) invert(35%) sepia(85%) saturate(1200%) hue-rotate(340deg) brightness(95%) contrast(90%);
}
</style>