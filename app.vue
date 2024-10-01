<script setup>

import '~/assets/css/index.css'


const medicos = reactive ([
  {
    nome: "Ana Silva",
    dataNascimento: "1985-06-15",
    email: "ana.silva@example.com",
    telefone: "(11) 98765-4321",
    numeroRegistroProfissional: "CRP-12345",
    disorder: "autismo"
    crp: "CRP-12345",
    desordem: "autismo"
  },
  {
    nome: "Carlos Souza",
    nascimento: "1990-04-22",
    email: "carlos.souza@example.com",
    telefone: "(21) 99876-5432",
    numeroRegistroProfissional: "CRP-67890",
    disorder: "depressao"
  },
  {
    nome: "Fernanda Oliveira",
    nascimento: "1982-11-30",
    email: "fernanda.oliveira@example.com",
    telefone: "(31) 91234-5678",
    numeroRegistroProfissional: "CRP-11223",
    disorder: "bipolaridade"
  },
  {
    nome: "João Pereira",
    nascimento: "1978-02-10",
    email: "joao.pereira@example.com",
    telefone: "(41) 93456-7890",
    numeroRegistroProfissional: "CRP-33445",
    disorder: "autismo"
  },
  {
    nome: "Maria Santos",
    nascimento: "1993-07-05",
    email: "maria.santos@example.com",
    telefone: "(51) 92345-6789",
    numeroRegistroProfissional: "CRP-55667",
    disorder: "depressao"
  },
  {
    nome: "Pedro Almeida",
    nascimento: "1988-01-17",
    email: "pedro.almeida@example.com",
    telefone: "(61) 99887-6655",
    numeroRegistroProfissional: "CRP-77889",
    disorder: "bipolaridade"
  },
  {
    nome: "Clara Lima",
    nascimento: "1980-09-29",
    email: "clara.lima@example.com",
    telefone: "(71) 91122-3344",
    numeroRegistroProfissional: "CRP-99000",
    disorder: "autismo"
  },
  {
    nome: "Ricardo Costa",
    nascimento: "1986-12-12",
    email: "ricardo.costa@example.com",
    telefone: "(81) 91234-5678",
    numeroRegistroProfissional: "CRP-22334",
    disorder: "depressao"
  },
  {
    nome: "Juliana Martins",
    nascimento: "1991-03-08",
    email: "juliana.martins@example.com",
    telefone: "(91) 93456-7890",
    numeroRegistroProfissional: "CRP-44556",
    disorder: "bipolaridade"
  },
  {
    nome: "Roberto Ferreira",
    nascimento: "1987-08-25",
    email: "roberto.ferreira@example.com",
    telefone: "(11) 97654-3210",
    numeroRegistroProfissional: "CRP-66778",
    disorder: "autismo"
  }
])

const usuarios = reactive([
    {
        nome: "João Silva",
        senha: "123",
        nascimento: "1990-05-15",
        email: "joao@email.com"
    },
    {
        nome: "Maria Oliveira",
        senha: "123",
        nascimento: "1985-10-20",
        email: "maria@email.com"
    },
    {
        nome: "Pedro Santos",
        senha: "123",
        nascimento: "1992-03-30",
        email: "pedro@email.com"
    },
    {
        nome: "Ana Costa",
        senha: "123",
        nascimento: "1995-07-25",
        email: "ana@email.com"
    },
    {
        nome: "Lucas Pereira",
        senha: "123",
        nascimento: "1988-12-01",
        email: "lucas@email.com"
    }
]);

const clinicas = reactive([
    {
        nomeClinica: "Clínica Saúde e Bem-Estar",
        cnpj: "12.345.678/0001-90",
        endereco: "Rua das Flores, 123",
        estado: "São Paulo",
        cidade: "São Paulo",
        cep: "01234-567",
        nomeUsuario: "clinica1",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica do Coração",
        cnpj: "98.765.432/0001-21",
        endereco: "Avenida Brasil, 456",
        estado: "Rio de Janeiro",
        cidade: "Rio de Janeiro",
        cep: "98765-432",
        nomeUsuario: "clinica2",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Vida Nova",
        cnpj: "11.222.333/0001-45",
        endereco: "Praça da Liberdade, 789",
        estado: "Minas Gerais",
        cidade: "Belo Horizonte",
        cep: "12345-678",
        nomeUsuario: "clinica3",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Família Feliz",
        cnpj: "44.555.666/0001-78",
        endereco: "Rua das Palmeiras, 101",
        estado: "Bahia",
        cidade: "Salvador",
        cep: "45678-901",
        nomeUsuario: "clinica4",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Saúde Plena",
        cnpj: "77.888.999/0001-32",
        endereco: "Avenida das Nações, 202",
        estado: "São Paulo",
        cidade: "São Paulo",
        cep: "23456-789",
        nomeUsuario: "clinica5",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Bem Estar",
        cnpj: "22.333.444/0001-56",
        endereco: "Rua do Sol, 303",
        estado: "Rio de Janeiro",
        cidade: "Rio de Janeiro",
        cep: "34567-890",
        nomeUsuario: "clinica6",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Esperança",
        cnpj: "55.666.777/0001-89",
        endereco: "Avenida da Saúde, 404",
        estado: "Paraná",
        cidade: "Curitiba",
        cep: "45612-345",
        nomeUsuario: "clinica7",
        senha: "senha123"
    },
    {
        nomeClinica: "Clínica Vitalidade",
        cnpj: "88.999.000/0001-12",
        endereco: "Rua do Comércio, 505",
        estado: "Rio Grande do Sul",
        cidade: "Porto Alegre",
        cep: "56789-012",
        nomeUsuario: "clinica8",
        senha: "senha123"
    }
]);



</script>


<template>
  
<Head>

<Script src="https://kit.fontawesome.com/e9b73e9254.js"></script>

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

    
<NuxtPage v-bind:medicos="medicos" v-bind:usuarios="usuarios" v-bind:clinicas="clinicas"/>


</template>
