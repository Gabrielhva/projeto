<script setup>

import '~/assets/css/login.css'

const params= defineProps(["usuarios"])

let email = ref("")
let senha = ref("")


    function enviaFormulario(){
            
        let usuario = {
            nome: "",
            senha: "",
            nascimento: "",
            email: ""
        };

        params.usuarios.map(u=>{
            if(u.email==email.value && u.senha==senha.value){
                usuario = u
            }
        })

        if(usuario.nome=="" || usuario.nome== null){
            alert("usuario não encontrado")
            return
        }

        alert("usuario logado com sucesso")

        localStorage.setItem("usuario", JSON.stringify(usuario))
    
    }

      

</script>

<template>

<hr/>
<section class="fundologin">
    <div class="divlogin">

        <h2 class="titulologin">Entrar com seu perfil</h2>
        <br/><br/>

        <p class="subtitulo"> Use sua conta para acessar seu painel de usuário </p>
        <br/>

        <p class="informacoespag"> Ainda nao tem uma conta? Cadastre-se agora mesmo,<NuxtLink to="/cadastro" class="clickaquilogin">clicando aqui. </NuxtLink></p> 
       
         
        
        <form v-on:submit.prevent="enviaFormulario()">

             <div class="campologin">
            <p> E-mail: </p>
           <input v-model="email"/>

            <br/>

            <p> Senha: </p>
            <input type="password" v-model="senha"/>
           
            </div>

            <button class="botaologin"> Entrar </button>
           
        </form>

    </div>

</section>


        

    
</template>