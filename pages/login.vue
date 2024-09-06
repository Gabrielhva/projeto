<script>



         function enviaFormulario(e){

            e.preventDefault();  
             
            const usuario = {

                nome:"",
                senha:""


            };

            usuario.nome = e.target.nome.value;
            usuario.senha = e.target.senha.value;

            console.log("nome:",usuario.nome);
            console.log("senha:",usuario.senha);

        if (usuario.nome == "admin"){

            console.log("Usuário correto");
        }

            else {


            console.log("Usuário incorreto!");


        }

        if (usuario.senha == "senha"){

            console.log("Senha correta");
            
        }

            else {

                console.log("Senha incorreta!");

            }



        
            }
</script>

<template>

<hr/>

        <h2> Entrar </h2>
        <br/><br/>

        <p> Use sua conta para acessar seu painel de usuário </p>
        <br/>

        <p> Ainda nao tem uma conta? Cadastre-se agora mesmo,<NuxtLink to="/cadastrar"> clicando aqui </NuxtLink></p> 
         <!-- depois validar -->
         <br/>

         <form action="/index">
            <p> E-mail: </p>
           <input/>

            <br/>

            <p> Senha: </p>
            <input/>
            <br/>
            <br/>

            <button> Entrar </button>
         
            <!-- dois validar button -->

        </form>

         

        


         

    <hr/>



    
</template>