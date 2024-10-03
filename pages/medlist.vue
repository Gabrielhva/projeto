<script setup>

import '~/assets/css/medlist.css'

const params = defineProps(["medicos"])

let mostrar = ref(1)

  function alteramostrar(valor){
    mostrar.value = valor
  }

</script>


<template>

<div class="container mx-auto mt-4 " >
    
  <div class="ajuste">

    <section v-for="medico in params.medicos">

      <div v-if="mostrar == medico.id">
        <div class="modalFade" v-on:click="alteramostrar(-1)"></div>
          <div class="modalConteudo">      
            <h2>
            {{ medico.nome }}
            </h2>
            <p>{{ medico.desordem }}</p>
            <p>{{ medico.email }}</p>
            <button v-on:click="alteramostrar(-1)">Fechar</button>

        </div>
      </div>
    <div class="col-md-4" >
      <div class="card" style="width: 18rem;">
      <img v-bind:src=" medico.foto " class="img_perfil_med" alt="...">

      <div class="card-body">
        <h5 class="card-title">{{ medico.nome }}</h5>
        <h6 class="tipomed">{{ medico.desordem }}</h6>
    
       <button v-on:click="()=>alteramostrar" class="btn mr-2"><i class="fa-solid fa-paper-plane"></i> Contatar</button>
       <button v-on:click="()=>alteramostrar(medico.id)" class="btn"><i class="fa-solid fa-envelope"></i>Email</button>

      </div>
    </div>
  </div> 

    </section>
    
   
    
        
  </div>
</div>




</template>


<style scoped>
  .modalFade{
    background: black;
    opacity: 0.5;
    position:fixed;
    left:0;
    top: 0;
    width: 100%;
    height: 100%;
    z-index: 100;
  }
  .modalConteudo{

    background: white;
    position: fixed;
    z-index: 200;
    text-align: center;
    width: 500px;
    transform: translate(-50%, -50%);
    left: 50%;
    top: 50%;
  }

  .card {
  margin-top: 10px;
  background: #222;
  border: 1px solid #19e6b9;
  color: rgba(250, 250, 250, 0.8);
  margin-bottom: 2rem;
  padding-bottom: 10px;
}
</style>