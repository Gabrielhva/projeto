<script setup> 

import '~/assets/css/cadastro.css'

const params = defineProps(["usuarios", "medicos","clinicas"])

let categoria = ref("usuarios")



function alteraFormulario(valor){
  categoria.value = valor
}

  const usuarioConvencional= reactive({

    nome:"",
    senha:"",
    nascimento:"",
    email:""

  })

  function criarUsuarioConvencional(){
    params.usuarios.push(usuarioConvencional)
    alert("Usuario criado com sucesso !")
    console.log(params.usuarios)
  }

  const medicos = reactive({

nome:"",
senha:"",
nascimento:"",
email:"",
telefone:"",
crp:"",
desordem:"",
  })

  function criarProfissional(){
    params.medicos.push(medicos)
    alert("Usuario profissional criado com sucesso !")
    console.log(params.medicos)
  }

  const clinicas = reactive({

    nomeClinica:"", 
    cnpj:"", 
    endereço:"", 
    estado:"",
    cidade:"",
    cep:"",
    nomeUsuario:"",
    senha:"",



  })

  function criarClinica(){
    params.clinicas.push(clinicas)
    alert("Clinica criado com sucesso !")
    console.log(params.clinicas)

  }





</script>



<template>


<h2 class="conteudoCadastro" >Cadastre-se</h2>


  <p class="ajusteCadastro">Escolha seu tipo de conta</p>
  
  

   <div class="ajustebotaoCadastro">

    <button class="botaoCadastro" v-on:click="alteraFormulario('usuario')">Usuario Convencional</button>

    <button class="botaoCadastro" v-on:click="alteraFormulario('profissional')">Suporte Profisional</button>
    
    <button class="botaoCadastro" v-on:click="alteraFormulario('clinica')">Clinicas Especializadas</button>

    

    </div >

   

    <form v-if="categoria =='usuario' " id="usuarioConvencional" v-on:submit.prevent="criarUsuarioConvencional()">


      <p class="conteudoCadastro"> 

        <label>
        Nome Completo:<input v-model="usuarioConvencional.nome">
        </label>
        
      </p>

      
      <p class="conteudoCadastro">

        <label>
          Data Nascimento:<input v-model="usuarioConvencional.nascimento">
        </label>

      </p>


      <p class="conteudoCadastro">

        <label>
          
          E-mail:<input v-model="usuarioConvencional.email">
        </label>

      </p>


      <p class="conteudoCadastro">

        <label>
          Senha:<input v-model="usuarioConvencional.senha">
        </label>

      </p>


      

        <label class="conteudoCadastro">
          <input type="checkbox" required/> Li e aceito os termos de uso
        </label>

      
                    

    <button class="botaoCadastro"> Cadastrar </button> <button class="botaoCadastro"> Cancelar </button>

    </form>



    <form v-if="categoria =='profissional'" id="suporteProfissional" v-on:submit.prevent="criarProfissional()">

      


        <p class="conteudoCadastro">

          <label>
          Nome Completo: <input v-model="medicos.nome">
          </label>

        </p>
       
       
      <p class="conteudoCadastro">

        <label>
        Data Nascimento: <input v-model="medicos.dataNascimento">
        </label>
      
      </p>


      <p class="conteudoCadastro">

      <label>
      E-mail: <input v-model="medicos.email">
      </label>

      </p>


      <p class="conteudoCadastro">

      <label>
      Telefone: <input v-model="medicos.telefone">
      </label>
     
     </p>


     <p class="conteudoCadastro">

        <label>
        Número de Registro Profissional (CRP): <input v-model="medicos.crp">
        </label>

     </p>

     <p class="conteudoCadastro">

    <label>
    Especialização: <input v-model="medicos.desordem">
   </label>

   <p class="conteudoCadastro">

   <label>
    Foto: <input img src="https://i.imgur.com/uaNj0Mb.png">
   </label>

  </p>


    </p>






    <label class="conteudoCadastro" >
    <input type="checkbox" required /> Li e aceito os termos de uso
    </label>
       

    <button class="botaoCadastro"> Cadastrar </button> <button class="botaoCadastro"> Cancelar </button>
  

      

      

    
</form>




<form v-if="categoria =='clinica'"id="clinicasEspecializadas"  v-on:submit.prevent="criarClinica()">


<p class="conteudoCadastro">

  <label>
Nome da clinica:<input  v-model="clinicas.nomeClinica">
 </label>

</p>

 
<p class="conteudoCadastro">

  <label>
CNPJ: <input v-model="clinicas.cnpj">
</label>


</p>



<p class="conteudoCadastro">

  <label>
Endereço :<input v-model="clinicas.endereco">
</label>


</p>



<p class="conteudoCadastro">

  <label>
Estado <input v-model="clinicas.estado">
</label>


</p>


<p class="conteudoCadastro">

  <label>
Cidade: <input v-model="clinicas.cidade">
</label>


</p>


<p class="conteudoCadastro">

  <label>
Cep: <input v-model="clinicas.cep">
</label>

</p>


<p class="conteudoCadastro">

  <label>
Nome do usuario: <input v-model="clinicas.nomeUsuario">
</label>



</p>


<p class="conteudoCadastro">

  <label>
Senha: <input v-model="clinicas.senha">
</label>



</p>



<label class="conteudoCadastro">
<input type="checkbox" required/> Li e aceito os termos de uso

</label>
       

<button class="botaoCadastro"> Cadastrar </button> <button class="botaoCadastro"> Cancelar </button>


      





</form>


  
</template>