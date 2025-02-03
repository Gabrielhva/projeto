

<script setup>



async function buscarmed () {
  const resposta = axios.get("http://10.60.44.45:3000/doctor/read")
  console.log(resposta)
}

import axios from 'axios'

async function buscardisorder () {
  const resposta = axios.get("http://10.60.44.23:3000/disorder/read")
  console.log(resposta)
}

let categoria = ref("depressao")

const medicos = reactive ([])

onMounted(
  () => {
    buscarmed()
  }
)

function alteraTopicos(valor){
  categoria.value = valor
}

function alteraMedico(valor){
  categoria.value = valor
}


</script>


<style scoped>
ul {
  margin-right: 30px;
  padding: 0;
  text-align: justify; /* Justifica o texto dentro da lista */
}

li {
  margin-bottom: 20px;
  background-color: rgb(167, 204, 195);
  color: rgb(75, 99, 85);
  padding: 10px;
  text-align: justify; /* Altera de center para justify */
  cursor: pointer;
  border-radius: 9px;
  font-family:monospace ;
  font-size: 20px;
}

li:hover {
 background-color: rgb(168, 219, 207);
  transition: 0.3s;
  text-align: justify; /* Altera de center para justify */
  color: rgb(255, 255, 255);
  background-color: rgb(142, 197, 189);
  transition: background-color 0.5s ease, color 0.5s ease, transform 0.5s ease;
  font-family:monospace ;
  font-size: 20px;
  white-space: nowrap;
  cursor:pointer;
  color: rgb(75, 99, 85);
}

.divisao {
  display: flex;
}

.topicos {
  text-align: center;
  width: 800px;
}

.conteudo {
  width: 100%;
  text-align: justify; /* Mantém o texto justificado */
  font-size: 18px;
  color: rgb(75, 99, 85);
  margin-left: 10px;
  margin-right: 35px;
}

.h2 {
  text-align: center !important;
  background: red;
}

.esquerda {
  text-align: justify; /* Altera de center para justify */
  font-size: 18px;
  color: rgb(75, 99, 85);
}

.body {
  font-family: 'Times New Roman', Times, serif;
}

div {
  text-align: justify; /* Altera de center para justify */
  color: rgb(75, 99, 85);
}

h1 {
  text-align: center;
}
</style>

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
      <li v-on:click="alteraTopicos('borderline')">Borderline</li>
      <li v-on:click="alteraTopicos('esquizofrenia')">Esquizofrenia</li>
      <li v-on:click="alteraTopicos('Transtorno de estresse pos traumatico')">Transtorno de Estresse Pós-Traumatico</li>
      <li v-on:click="alteraTopicos('Transtorno obsessivo-compulsivo')">Transtorno Obsessivo-Compulsivo</li>
      <li v-on:click="alteraTopicos('dependencia alcoolica')">Dependencia Alcoólica</li>
      <li v-on:click="alteraTopicos('dependenciadedrogasilicitas')">Dependencia de Drogas Ilícitas</li>
      <li v-on:click="alteraTopicos('dependenciademedicamentos')">Dependencia de Medicamentos</li>
    </ul>

    <div v-if="categoria=='autismo'">

      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='autismo'"  v-bind:medicos="medico" />
      </div>

    </div>


    <div v-if="categoria=='depressao'">

      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='depressão'"  v-bind:medicos="medico" />
      </div>  
  
    </div>


    <div v-if="categoria=='bipolaridade'">

<div v-for="medico in medicos" >
    <TopicosMedicos v-if=" medico.desordem=='bipolaridade'"  v-bind:medicos="medico" />
</div>  

</div>

  

    
    <div v-if="categoria=='borderline'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='borderline'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='esquizofrenia'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='esquizofrenia'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='Transtorno de estresse pos traumatico'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='Transtorno de estresse pos traumatico'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='Transtorno obsessivo-compulsivo'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='Transtorno obsessivo-compulsivo'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependencia alcoolica'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='dependencia alcoolica'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependenciadedrogasilicitas'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='dependenciadedrogasilicitas'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependenciademedicamentos'">
      
      <div v-for="medico in medicos" >
          <TopicosMedicos v-if=" medico.desordem=='dependenciademedicamentos'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>



  </div>


  <div class="conteudo">



    <div v-if="categoria=='autismo'"><TopicosAutismo/></div>
    <div v-if="categoria=='depressao'"><TopicosDepressao/></div>
    <div v-if="categoria=='bipolaridade'"><TopicosBipolaridade/></div>
    <div v-if="categoria=='borderline'"><TopicosBorderline/></div>
    <div v-if="categoria=='esquizofrenia'"><TopicosEsquizofrenia/></div>
    <div v-if="categoria=='Transtorno de estresse pos traumatico'"><TopicosTranstornodeestressepostraumatico/></div>
    <div v-if="categoria=='Transtorno obsessivo-compulsivo'"><TopicosTranstornoobsessivo-compulsivo/></div>
    <div v-if="categoria=='dependencia alcoolica'"><TopicosDepedenciaalcoolica/></div>
    <div v-if="categoria=='dependenciadedrogasilicitas'"><TopicosDependenciadedrogasilicitas/></div>
    <div v-if="categoria=='dependenciademedicamentos'"><TopicosDependenciademedicamentos/></div>
    
    



  </div>
    
</div>
  
    
</template>
