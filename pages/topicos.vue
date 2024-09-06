

<script setup>

let categoria = ref("depressao")

function alteraTopicos(valor){
  categoria.value = valor
}



</script>

<template>
<div class="divisao">
<hr>
  <div class="topicos">
  <hr>
    <p> <strong>Topicos</strong></p>
    <ul>
      <li v-on:click="alteraTopicos('autismo')" >Autismo</li>
      <li v-on:click="alteraTopicos('depressao')">Depressão</li>
      <li v-on:click="alteraTopicos('bipolaridade')">Bipolaridade</li>
      <li v-on:click="alteraTopicos('boderlaine')">Boderlaine</li>
      <li v-on:click="alteraTopicos('esquizofrenia')">Esquizofrenia</li>
      <li v-on:click="alteraTopicos('Transtorno de estresse pos traumatico')">Transtorno de estresse pós-traumatico</li>
      <li v-on:click="alteraTopicos('Transtorno obcessivo-compulsivo')">Transtorno Obcessivo-compulsivo</li>
      <li v-on:click="alteraTopicos('depedencia alcolica')">Depedencia Alcoólica</li>
      <li v-on:click="alteraTopicos('depedencia de drogas ilicitas')">Depedencia de Drogas Ilicitas</li>
      <li v-on:click="alteraTopicos('depedencia de medicamentos')">Depedencia de Medicamentos</li>
    </ul>

  </div>


  <div class="conteudo">

    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    <div v-if="categoria=='depressao'"><TopicosDepressao/></div>
    <div v-if="categoria=='bipolaridade'"><TopicosBipolaridade/></div>
    <div v-if="categoria=='boderlaine'"><TopicosBoderlaine/></div>
    <div v-if="categoria=='esquizofrenia'"><TopicosEsquizofrenia/></div>
    <div v-if="categoria=='Transtorno de estresse pos traumatico'"><TopicosTranstornodeestressepostraumatico/></div>
    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    
    



  </div>
    
</div>
  
    
</template>

<style scoped>

ul{
  margin-right: 30px;
  padding: 0;
}

li{
  margin-bottom: 20px;
  background: green;
  color: white;
  padding: 10px;
  text-align: center;
  cursor: pointer;
}
li:hover{
  background: darkgreen;
  transition: 0.3s;
}

.divisao{
  display: flex;
}
.topicos{
  text-align: center;
  width: 800px;
}

.conteudo{
  width: 100%;
}

</style>