<script setup>

import '~/assets/css/assinatura.css'

</script> 

<template>
    
<h1 class="tituloo">Atenda muito mais com Premium <i class="fa-solid fa-bolt"></i></h1>

<section class="fundoo">


<div class="containerr">

    

        <img class="imga" src="/public/black.jpg"/>

        <img class="imga" src="/public/black.jpg"/>
        
    

    <div class="texto-sobre-imagem">

    <div class="textoo textoo2"><strong>Versão para Especialistas <i class="fa-solid fa-notes-medical"></i></strong></div>
    <div class="textoo textoo3"><strong>Doenças Mentais</strong></div>
    <div class="textoo espacoo"><strong>R$ 49,99 <p class="textoo4">/Mês</p></strong></div>
    <div class="textoo textoo5"><strong><span class="spann">✓</span> Destaque para os pacientes</strong></div>
    <div class="textoo textoo6"><strong><span class="spann">✓</span> Perfil mais personalizado</strong></div>
    <div class="textoo textoo7"><strong><span class="spann">✓</span> Maior taxa de resposta</strong></div>

     <NuxtLink :to="{ path: '/pagamento', query: { tipo: 'doctor' } }"> <div class="textoo botaoo"><button class="buttonn">Assinar</button> </div> </NuxtLink>
    


    </div>
    <div class="containerr2">
    <div class="texto-sobre-imagem">


    <div class="textoo textoo2"><strong>Versão para Clínicas <i class="fa-solid fa-house-medical"></i></strong></div>
    <div class="textoo textoo3"><strong>Dependência Química</strong></div>
    <div class="textoo espacoo"><strong>R$ 119,99 <p class="textoo4">/Mês</p></strong></div>
    <div class="textoo textoo5"><strong><span class="spann">✓</span> Destaque para os pacientes</strong></div>
    <div class="textoo textoo6"><strong><span class="spann">✓</span> Layout de Clínica personalizado</strong></div>
    <div class="textoo textoo7"><strong><span class="spann">✓</span> Maior taxa de resposta</strong></div>
    
     <NuxtLink :to="{ path: '/pagamento', query: { tipo: 'clinic' } }"> <div class="textoo botaoo"><button class="buttonn">Assinar</button></div> </NuxtLink>
    </div>
    </div>

</div>
</section>
</template>