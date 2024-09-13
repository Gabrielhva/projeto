<script>

import '~/assets/css/index.css'


</script>


<template>
  
<Head>

<Script src="https://kit.fontawesome.com/e9b73e9254.js">



</Script>

</Head>
 

<div class="container">
    
    <img src="./public/logo.png" alt="logo" class="logo"/>

    <NuxtLink to="/"> <button class="botao ajuste">Inicio</button></NuxtLink> 
    <NuxtLink to="/recursos"><button class="botao">Recursos</button></NuxtLink>  
    <NuxtLink to="/quemsomos"> <button class="botao">Quem Somos</button></NuxtLink>
    <NuxtLink to="/topicos"> <button class="botao">Tópicos</button></NuxtLink>
    <NuxtLink to="/login"><button class="botao">Entrar</button></NuxtLink>

    <div class="search-box ajustebusca">
    <button class="btn-search"><i class="fa-solid fa-magnifying-glass"></i></button>
    <input type="text" class="input-search" placeholder="Buscar...">
    </div>

    
    <p class="distperfil">Perfil</p><button type="button" class="perfil">
    <img src="/public/user1.png" class="fotoperfil"></button>
   

    </div>

    <!--<section class="bg">-->

    
<NuxtPage/>


</template>
