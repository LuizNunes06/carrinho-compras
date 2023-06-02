<script setup>
import {livros} from '@/_data/livros'
</script>

<template>
  <h1 class="livro-titulo">Minha Livraria</h1>
  <div class="listagem-livros">
   <div v-for="livro in livros" :key="livro.id" class="card-livro">
    <img :src="livro.cover" alt="capa" class="livro-capa">
    <p class="livro-titulo"> {{ livro.title }}</p>
    <p class="livro-autor"> {{ livro.author }}</p>
    <p class="livro-preco"> {{ livro.price }}</p>
  </div>
    
  </div>
</template>

<style scoped>
.livro-capa{
  width: 200px;
}
.card-livro{
  background-color: rgb(197, 196, 255);
  padding: 10px;
  border-radius: 10px;
  width: 200px;
  margin: 10px;
}
.listagem-livros{
display: flex;
flex-wrap: wrap;
justify-content: space-around;
}
h1{
  text-align: center;
  color:  rgb(47, 46, 107);
  margin: 50px;
}
.listagem-livros .livro-titulo{
  font-weight: bold;
}


</style>
