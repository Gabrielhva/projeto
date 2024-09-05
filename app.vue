<template>
  

 

<div class="container">
    <img src="./imagens/logo.png" alt="logo" class="logo"/>

    <NuxtLink to="/"> <button class="botao ajuste">Inicio</button></NuxtLink> 
    <NuxtLink to="/recursos"><button class="botao">Recursos</button></NuxtLink>  
    <NuxtLink to="/quemsomos"> <button class="botao">Quem Somos</button></NuxtLink>
    <NuxtLink to="/topicos"> <button class="botao">Tópicos</button></NuxtLink>
    <NuxtLink to="/login"><button class="botao">Entrar</button></NuxtLink>

    <p class="distperfil">Perfil</p><button type="button" class="perfil">
    <img src="./imagens/user1.png" class="fotoperfil"></button>
    
    </div>

    <!--<section class="bg">-->

    <div id="divbusca">

        <input type="text" id="txtbusca" placeholder="Buscar..."/>

        <img src="./imagens/magnifying-glass-solid.svg" class="lupaimg" id="btnlupa" alt="lupa"/>

    </div>
    
<NuxtPage/>


</template>
