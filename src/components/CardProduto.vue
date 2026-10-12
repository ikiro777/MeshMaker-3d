<script setup>
const props = defineProps({
titulo:String,
valor: Number,
descricao: String,
categoria: String,
imagem: String,
})

</script>


<template>
  <div class ="principal">
  <h2>{{categoria}}</h2>
      <span><img class="imagem":src="imagem" :alt="titulo"></span>
      <span>{{titulo}}</span>
      <span class= "descricao">{{descricao}}</span>
      <strong><span class="valorproduto">{{valor}}</span></strong>
  </div>

</template>


<style scoped>
  .principal {
    border: 1px, solid #1122;
    border-radius: 8px;
    margin: 25px;
    padding: 10px;
    justify-content: space-between;
    display: flex;
    flex: 1;
    min-width: 170px; 
    max-width: 250px;
    height: 100%;
    max-height: 350px;
    flex-direction: column;
    background: white; 
    color: black;
    transition: all 0.3s ease;
  
  } 
  
  .principal:hover{
  background-color: #f0f0f0;
  border-color: #f00000;
  transform: translateY(-4px);
  box-shadow: 0px 8px 16px rgba(0, 0, 0, 0.1)
  
  }
  
  .imagem {
    width:100%;
    height:100%;
    max-height: 200px;
    max-width: 200px;
  }.valorproduto {
    font-weight: 1px;
  } .descricao {
    color: grey;
  }
  h2{
    color:black;
  }
</style>