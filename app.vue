<script setup>

import '~/assets/css/index.css'

</script>


<template>
  
<Head>

<Script src="https://kit.fontawesome.com/e9b73e9254.js"></Script>

</Head>
 

<div class="container">
    
    <img src="./public/logo.png" alt="logo" class="logo"/>
    
    <NuxtLink to="/"> <button class="botaoaaa ajuste">Inicio</button></NuxtLink> 
    <NuxtLink to="/recursos"><button class="botaoaaa">Recursos</button></NuxtLink>  
    <NuxtLink to="/quemsomos"> <button class="botaoaaa">Quem Somos</button></NuxtLink>
    <NuxtLink to="/topicos"> <button class="botaoaaa">Tópicos</button></NuxtLink>
    <NuxtLink to="/login"><button class="botaoaaa">Entrar</button></NuxtLink>
  

    

    
    <p class="distperfil">Perfil</p><NuxtLink to="/meuperfil"><button type="button" class="perfil">
    
    <img src="/public/user1.png" class="fotoperfil"></button></NuxtLink>
    

    </div>

    <!--<section class="bg">-->

    
<NuxtPage v-bind:medicos="medicos"/>


</template>
