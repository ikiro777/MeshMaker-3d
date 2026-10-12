<script setup>
defineProps({
  titulo: String
})
</script>

<template>
  <header class="header">
   <img src="/MeshMakerLogo.svg">
    <div class="texto">O lugar onde sua criatividade surge em formato 3D</div>
  </header>
</template>

<style scoped>

img {
  width:200px;
}
.texto {
  align-self: center;
}
.header {
  background-color: coral;
  color: white;
  padding: 2px;
  gap: 30px;
  min-width: 150px;
  display: flex;
  justify-content: space-between;
  padding-left: 20px;
  padding-right: 20px;
  
}

.header h1 {
  margin: 0;
  font-size: 1.5rem;
}

.header p {
  margin-bottom: 0;
}
</style>