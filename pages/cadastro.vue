<script setup> 

  import '~/assets/css/cadastro.css'
  import axios from 'axios'


  const params = defineProps()

  let categoria = ref("usuarios")



  function alteraFormulario(valor){
    categoria.value = valor
  }

  const usuarioConvencional= reactive({
    nome:"",
    senha:"",
    nascimento:"",
    email:"",
    type:"comum"
  })

  async function criarUsuarioConvencional(){
    try{
      const resposta = await axios.post("http://10.60.44.28:3001/doctor/create", usuarioConvencional)
      alert(resposta.data.message)
    } catch (error) {
      alert(error.response.message)
    }
    
  }

  const medicos = reactive({
    nome:"",
    senha:"",
    nascimento:"",
    senha:"",
    email:"",
    telefone:"",
    crp:"",
    desordem:"",
    type:"doctor",
    foto:""
  })

  async function criarProfissional(){
    //params.medicos.push(medicos)
    try{
      const resposta = await axios.post("http://10.60.44.28:3001/doctor/create", medicos)
      alert(resposta.data.message)
    } catch (error) {
      alert(error.response ? error.response.data.message : "Erro desconhecido");
    }
  }

  const clinicas = reactive({
    nomeClinica:"", 
    cnpj:"", 
    endereço:"", 
    nascimento:"",
    estado:"",
    cidade:"",
    cep:"",
    nome:"",
    email:"",
    senha:"",
    type:"clinica"
  })

  async function criarClinica(){
    try{
      const resposta = await axios.post("http://10.60.44.28:3001/doctor/create", clinicas)
      alert(resposta.data.message)
    } catch (error) {
      alert(error.response.message)
    }
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
        Data Nascimento: <input v-model="medicos.nascimento">
        </label>
      
      </p>


      <p class="conteudoCadastro">

      <label>
      E-mail: <input v-model="medicos.email">
      </label>

      </p>

      <p class="conteudoCadastro">

         <label>
           Senha: <input v-model="medicos.senha">
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
    </p>

    <p class="conteudoCadastro">

      <label>
        Foto: <input v-model="medicos.foto">
      </label>

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
  Data de Fundação: <input v-model="clinicas.nascimento">
</label>

</p>


<p class="conteudoCadastro">

  <label>
Endereço: <input v-model="clinicas.endereco">
</label>


</p>



<p class="conteudoCadastro">

  <label>
Estado: <input v-model="clinicas.estado">
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
Nome do usuario: <input v-model="clinicas.nome">
</label>



</p>

<p class="conteudoCadastro">

<label>
E-mail: <input v-model="clinicas.email">
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