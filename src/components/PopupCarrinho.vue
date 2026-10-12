<script setup>
defineProps({
  itens: Array,
  total: String,
})

defineEmits(['fechar', 'remover', 'comprar'])
</script>

<template>
  <div class="fundo-overlay" @click.self="$emit('fechar')">
    <div class="principal">
      <img src="/close.svg" class="iconeclose" @click="$emit('fechar')">
      <header>
        <h1>Seu carrinho</h1>
      </header>

      <div class="conteudo">
        <p v-if="itens.length === 0">Seu carrinho está vazio.</p>
        <ul v-else>
          <li v-for="item in itens" :key="item.titulo">
            {{ item.quantidade }}x {{ item.titulo }} — {{ item.valor }}
            <span @click="$emit('remover', item.titulo)">✕</span>
          </li>
        </ul>
      </div>

      <p><strong>Total: {{ total }}</strong></p>
      <button @click="$emit('comprar')"><strong>Comprar</strong></button>
    </div>
  </div>
</template>

<style scoped>
  .fundo-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: 9998;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  header{
  margin-bottom: 15px;  
    
  }
  .principal {
    position:relative;
    background-color: white;
    padding:30px;
    border-radius: 12px;
    box-shadow: 0px 10px 25px rgba(0, 0, 0, 0.3);
    width: 90%;
    max-width:400px;
    height: 80%;
    max-height: 500px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  } 

  .conteudo {
    border: 2px solid lightgrey;
    border-radius:6px;
    flex: 1;
    display: flex;
    justify-content: space-between; 
    align-items: center;     
    flex-direction: column;
  }
  

  button {
  background-color: #454ade;
  color: white;
  border-style: none;
  width: 50%; 
  height: 40px;
  margin-top: 20px;
  align-self: center;
  font-size: 15px;
  cursor:pointer;
  transition: all 0.3s ease;
  border-radius: 5px;
  }
  button:hover{
  background-color: #252AD0;
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.1)
  
  }


  .valorproduto {
    font-weight: 1px;
  } 
  
  .descricao {
    color: grey;
  }

  h1 {
    color:black;
    margin:0px;
    margin-bottom: 20px;
  }

  .cart {
    width:50px;
    height:50px;
    color: black;
  }

  .iconeclose{
    position: absolute;
    top: 15px;
    right: 15px;
    width: 24px;
    height: 24px;
    width: 24px;
    height: 24px;
    max-width: 35px;
    flex: 1;
    flex-shrink:0;
    transition: all 0.3s ease;
  }

  .iconeclose:hover{
    transform: scale(1.5);
    filter: brightness(0) saturate(100%) invert(35%) sepia(85%) saturate(1200%) hue-rotate(340deg) brightness(95%) contrast(90%);
  }
</style>