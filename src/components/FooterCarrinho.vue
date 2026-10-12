<script setup>
defineProps({
  valortotal: String,
  quantidadeitem: String,
});

const emit = defineEmits(['abrir'])

function abrirCarrinho() {
  emit('abrir')
}
</script>

<template>
  <div class="campo">
    <div class="divpai">
      <p>Total da compra</p>
      <span><strong>{{ valortotal }}</strong></span>
      /
      {{ quantidadeitem }}
    </div>

    <div class="divmae">
      <button @click="abrirCarrinho"><strong>Ver carrinho <img src="/triangle-up.svg" class="triangle-icon">
      </strong></button>
    </div>
  </div>
</template>

<style scoped>
.campo {
  position: fixed;
  bottom: 0;
  left: 0px;
  right: 0px;
  z-index: 1000;
  min-width: 150px;
  display: flex;
  justify-content: space-between;

  border-top: 2px solid;
  background-color: white;
  color: #454ade;
  padding-left: 20px;
  padding-right: 20px;
  padding-bottom: 15px;
  padding-top: 8px;
  gap: 30px;
}

.divpai {
  text-align: center;
  padding: 0px;
  flex:1;
}

.divpai h3 {
  margin: 0px;
}
.divmae {
  display: flex;
}

.divmae button {
  color: white;
  background-color: #454ade;
  flex:1;
  padding: 14px;
  font-size: 18px;
  border-radius: 4px;
  border-style: none;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  gap: px;
}

button:hover {
  background-color: #4A27C0;
  color: white;
}

.traço {
  color: white;
  background-color: #454ade;
  flex:1;
  border-radius: 4px;
}
.triangle-icon {
  filter: brightness(0) invert(1);
  width:15px;
  height:15px;
}
</style>