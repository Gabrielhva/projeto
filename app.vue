<script>

import '~/assets/css/index.css'


</script>


<template>
  

 

<div class="container">
    
    <img src="./public/logo.png" alt="logo" class="logo"/>

    <NuxtLink to="/"> <button class="botao ajuste">Inicio</button></NuxtLink> 
    <NuxtLink to="/recursos"><button class="botao">Recursos</button></NuxtLink>  
    <NuxtLink to="/quemsomos"> <button class="botao">Quem Somos</button></NuxtLink>
    <NuxtLink to="/topicos"> <button class="botao">Tópicos</button></NuxtLink>
    <NuxtLink to="/login"><button class="botao">Entrar</button></NuxtLink>

    <p class="distperfil">Perfil</p><button type="button" class="perfil">
    <img src="/public/user1.png" class="fotoperfil"></button>
    
    </div>

    <!--<section class="bg">-->
<div class="search-box">
    <button class="btn-search"><i class="fas fa-search"></i></button>
    <input type="text" class="input-search" placeholder="Type to Search...">
</div>
    
<NuxtPage/>


</template>
