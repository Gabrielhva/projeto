

<script setup>

let categoria = ref("depressao")

const params = defineProps(["medicos"])


function alteraTopicos(valor){
  categoria.value = valor
}

function alteraMedico(valor){
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
      <li v-on:click="alteraTopicos('borderline')">Borderline</li>
      <li v-on:click="alteraTopicos('esquizofrenia')">Esquizofrenia</li>
      <li v-on:click="alteraTopicos('Transtorno de estresse pos traumatico')">Transtorno de estresse pós-traumatico</li>
      <li v-on:click="alteraTopicos('Transtorno obsessivo-compulsivo')">Transtorno Obsessivo-compulsivo</li>
      <li v-on:click="alteraTopicos('dependencia alcoolica')">Dependencia alcoolica</li>
      <li v-on:click="alteraTopicos('dependenciadedrogasilicitas')">Dependencia de Drogas Ilicitas</li>
      <li v-on:click="alteraTopicos('dependenciademedicamentos')">Dependencia de Medicamentos</li>
    </ul>

    <div v-if="categoria=='autismo'">

      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='autismo'"  v-bind:medicos="medico" />
      </div>

    </div>


    <div v-if="categoria=='depressao'">

      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='depressao'"  v-bind:medicos="medico" />
      </div>  
  
    </div>


    <div v-if="categoria=='bipolaridade'">

<div v-for="medico in medicos" >
    <Medicos v-if=" medico.disorder=='bipolaridade'"  v-bind:medicos="medico" />
</div>  

</div>

    

    
    <div v-if="categoria=='borderline'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='borderline'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='esquizofrenia'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='esquizofrenia'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='Transtorno de estresse pos traumatico'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='Transtorno de estresse pos traumatico'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='Transtorno obsessivo-compulsivo'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='Transtorno obsessivo-compulsivo'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependencia alcoolica'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='dependencia alcoolica'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependenciadedrogasilicitas'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='dependenciadedrogasilicitas'"  v-bind:medicos="medico" />
      </div>
      
      
    </div>

    <div v-if="categoria=='dependenciademedicamentos'">
      
      <div v-for="medico in medicos" >
          <Medicos v-if=" medico.disorder=='dependenciademedicamentos'"  v-bind:medicos="medico" />
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

<style scoped>

ul{
  margin-right: 30px;
  padding: 0;
}

li{
  margin-bottom: 20px;
  background: rgb(5, 179, 135);
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