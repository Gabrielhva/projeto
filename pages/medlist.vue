<script setup>

import '~/assets/css/medlist.css'

const params = defineProps(["medicos"])

</script>


<template>
<section class="bg">
<div class="container mx-auto mt-4 " >
    
  <div class="ajuste">
    <section v-for="medico in medicos">
    <div class="col-md-4" >
      <div class="card" style="width: 18rem;">
  <img src="https://i.imgur.com/ZTkt4I5.jpg" class="img_perfil_med" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{ medico.nome }}</h5>
        <h6 class="tipomed">{{ medico.desordem }}</h6>
    <p class="card-text">Psiquiatra com 10 anos de experiência, Dr. Gabriel Henrique oferece atendimento empático e individualizado, especializado em psicofarmacologia e terapia cognitivo-comportamental.</p>
       <NuxtLink to="#" class="btn mr-2"><i class="fa-solid fa-paper-plane"></i> Contatar</NuxtLink>
       <NuxtLink to="#" class="btn"><i class="fa-solid fa-envelope"></i>Email</NuxtLink>
  </div>
  </div>
  </div>    
    </section>
    
   
    
        
    </div>
    </div>
</section>



</template>