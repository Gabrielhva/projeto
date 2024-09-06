<script setup>

let categoria = ref("usuario")

function alteraFormulario(valor){
  categoria.value = valor
  
}

</script>



<template>


<h2>Cadastre-se</h2>


  <p>Escolha seu tipo de conta</p>
  
  

   <div>

    <button v-on:click="alteraFormulario('usuario')">Usuario Convencional</button>

    <button v-on:click="alteraFormulario('profissional')">Suporte Profisional</button>
    
    <button v-on:click="alteraFormulario('clinica')">Clinicas Especializadas</button>

    

    </div>

   

    <form v-if="categoria =='usuario' " id="usuarioConvencional">


      <p> 

        <label>
        Nome Completo:<input>
        </label>
        
      </p>

      
      <p>

        <label>
          Data Nascimento:<input>
        </label>

      </p>


      <p>

        <label>
          
          E-mail:<input>
        </label>

      </p>


      <p>

        <label>
          Senha:<input>
        </label>

      </p>


      

        <label>
          <input type="checkbox" required/> Li e aceito os termos de uso
        </label>

      
                    

    <button> Cadastrar </button> <button> Cancelar </button>

    </form>



    <form form v-if="categoria =='profissional'" id="suporteProfissional">

      


        <p>

          <label>
          Nome Completo:<input>
          </label>

        </p>
       
       
      <p>

        <label>
        Data Nascimento: <input>
        </label>
      
      </p>


      <p>

      <label>
      E-mail:<input>
      </label>

      </p>


      <p>

      <label>
      Telefone: <input>
      </label>
     
     </p>


     <p>

        <label>
        Número de Registro Profissional (CRP): <input>
        </label>

     </p>

     <p>

    <label>
    Especialização:<input>
   </label>


    </p>






    <label>
    <input type="checkbox" required/> Li e aceito os termos de uso
    </label>
       

    <button> Cadastrar </button> <button> Cancelar </button>
  

      

      

    
</form>




<form form v-if="categoria =='clinica'"id="clinicasEspecializadas">


<p>

  <label>
Nome da clinica:<input>
 </label>

</p>

 
<p>

  <label>
CNPJ: <input>
</label>


</p>



<p>

  <label>
Endereço :<input>
</label>


</p>



<p>

  <label>
Estado <input>
</label>


</p>


<p>

  <label>
Cidade: <input>
</label>


</p>


<p>

  <label>
Cep: <input>
</label>

</p>


<p>

  <label>
Nome do ususario: <input>
</label>



</p>


<p>

  <label>
Senha: <input>
</label>



</p>



<label>
<input type="checkbox" required/> Li e aceito os termos de uso

</label>
       

<button> Cadastrar </button> <button> Cancelar </button>


      





</form>


  
</template>