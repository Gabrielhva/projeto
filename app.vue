<script setup>

import '~/assets/css/index.css'

const medicos = reactive([
  {
    id: 1,
    nome: "Clara Lima",
    dataNascimento: "1985-06-15",
    email: "ana.silva@example.com",
    telefone: "(11) 98765-4321",
    crp: "CRP-12345",
    desordem: "Autismo",
    foto: "https://i.imgur.com/gciGygV.png"
  },
  {
    id: 2,
    nome: "Ana Silva",
    dataNascimento: "1990-04-22",
    email: "carlos.souza@example.com",
    telefone: "(21) 99876-5432",
    crp: "CRP-67890",
    desordem: "Depressão",
    foto: "https://i.imgur.com/uaNj0Mb.png"
  },
  {
    id: 3,
    nome: "Fernando Oliveira",
    dataNascimento: "1982-11-30",
    email: "fernanda.oliveira@example.com",
    telefone: "(31) 91234-5678",
    crp: "CRP-11223",
    desordem: "Bipolaridade",
    foto: "https://i.imgur.com/LVW3J1R.png"
  },
  {
    id: 4,
    nome: "João Pereira",
    dataNascimento: "1978-02-10",
    email: "joao.pereira@example.com",
    telefone: "(41) 93456-7890",
    crp: "CRP-33445",
    desordem: "Autismo",
    foto: "https://i.imgur.com/yJv283w.png"
  },
  {
    id: 5,
    nome: "Maria Santos",
    dataNascimento: "1993-07-05",
    email: "maria.santos@example.com",
    telefone: "(51) 92345-6789",
    crp: "CRP-55667",
    desordem: "Depressão",
    foto: "https://i.imgur.com/RT9IIAA.png"
  },
  {
    id: 6,
    nome: "Juliana D'Santi",
    dataNascimento: "1988-01-17",
    email: "pedro.almeida@example.com",
    telefone: "(61) 99887-6655",
    crp: "CRP-77889",
    desordem: "Esquizofrenia",
    foto: "https://i.imgur.com/38iLu9a.png"
  },
  {
    id: 7,
    nome: "Carlos Estavan",
    dataNascimento: "1980-09-29",
    email: "clara.lima@example.com",
    telefone: "(71) 91122-3344",
    crp: "CRP-99000",
    desordem: "Autismo",
    foto: "https://i.imgur.com/D6Adccw.png"
  },
  {
    id: 8,
    nome: "Ricardo Costa",
    dataNascimento: "1986-12-12",
    email: "ricardo.costa@example.com",
    telefone: "(81) 91234-5678",
    crp: "CRP-22334",
    desordem: "Depressão",
    foto: "https://i.imgur.com/z6ldqU8.png"
  },
  {
    id: 9,
    nome: "Juliana Martins",
    dataNascimento: "1991-03-08",
    email: "juliana.martins@example.com",
    telefone: "(91) 93456-7890",
    crp: "CRP-44556",
    desordem: "Bipolaridade",
    foto: "https://i.imgur.com/vHHEEMd.png"
  },
  {
    id: 10,
    nome: "Roberto Ferreira",
    dataNascimento: "1987-08-25",
    email: "roberto.ferreira@example.com",
    telefone: "(11) 97654-3210",
    crp: "CRP-66778",
    desordem: "Ansiedade",
    foto: "https://i.imgur.com/7Lb03sQ.png"
  }
]);





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
      <input type="text" class="input-search" placeholder="Buscar..."/>
    </div>

    
    <p class="distperfil">Perfil</p><button type="button" class="perfil">
    
    <img src="/public/user1.png" class="fotoperfil"></button>
    

    </div>

    <!--<section class="bg">-->

    
<NuxtPage v-bind:medicos="medicos"/>


</template>
