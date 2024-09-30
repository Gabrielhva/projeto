<script setup>

import '~/assets/css/index.css'

const medicos = reactive ([
  {
    nome: "Ana Silva da Silva",
    dataNascimento: "1985-06-15",
    email: "ana.silva@example.com",
    telefone: "(11) 98765-4321",
    numeroRegistroProfissional: "CRP-12345",
    disorder: "autismo"
  },
  {
    nome: "Carlos Souza",
    dataNascimento: "1990-04-22",
    email: "carlos.souza@example.com",
    telefone: "(21) 99876-5432",
    numeroRegistroProfissional: "CRP-67890",
    disorder: "depressao"
  },
  {
    nome: "Fernanda Oliveira",
    dataNascimento: "1982-11-30",
    email: "fernanda.oliveira@example.com",
    telefone: "(31) 91234-5678",
    numeroRegistroProfissional: "CRP-11223",
    disorder: "bipolaridade"
  },
  {
    nome: "João Pereira",
    dataNascimento: "1978-02-10",
    email: "joao.pereira@example.com",
    telefone: "(41) 93456-7890",
    numeroRegistroProfissional: "CRP-33445",
    disorder: "autismo"
  },
  {
    nome: "Maria Santos",
    dataNascimento: "1993-07-05",
    email: "maria.santos@example.com",
    telefone: "(51) 92345-6789",
    numeroRegistroProfissional: "CRP-55667",
    disorder: "depressao"
  },
  {
    nome: "Pedro Almeida",
    dataNascimento: "1988-01-17",
    email: "pedro.almeida@example.com",
    telefone: "(61) 99887-6655",
    numeroRegistroProfissional: "CRP-77889",
    disorder: "bipolaridade"
  },
  {
    nome: "Clara Lima",
    dataNascimento: "1980-09-29",
    email: "clara.lima@example.com",
    telefone: "(71) 91122-3344",
    numeroRegistroProfissional: "CRP-99000",
    disorder: "autismo"
  },
  {
    nome: "Ricardo Costa",
    dataNascimento: "1986-12-12",
    email: "ricardo.costa@example.com",
    telefone: "(81) 91234-5678",
    numeroRegistroProfissional: "CRP-22334",
    disorder: "depressao"
  },
  {
    nome: "Juliana Martins",
    dataNascimento: "1991-03-08",
    email: "juliana.martins@example.com",
    telefone: "(91) 93456-7890",
    numeroRegistroProfissional: "CRP-44556",
    disorder: "bipolaridade"
  },
  {
    nome: "Roberto Ferreira",
    dataNascimento: "1987-08-25",
    email: "roberto.ferreira@example.com",
    telefone: "(11) 97654-3210",
    numeroRegistroProfissional: "CRP-66778",
    disorder: "autismo"
  }
])

</script>


<template>
  
<Head>

<Script src="https://kit.fontawesome.com/e9b73e9254.js"></Script>

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

    
<NuxtPage v-bind:medicos="medicos"/>


</template>
