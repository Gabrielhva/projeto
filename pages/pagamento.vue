<script setup> 

import '~/assets/css/pagamento.css'
import { useRoute } from 'vue-router'

const params = defineProps(["credito", "qrcode"])

const route = useRoute()
const valorFromQuery = (route.query.tipo === 'doctor')? 49.99 : 119.99

let categoria = ref("credito")



function alteraOpcaopagamento(valor){
  categoria.value = valor
}

  const infcreditos= reactive({
    nome:"",
    numeroCartao:"",
    cpf:"",
    validade:"",
    codigoSeguranca:"",
    parcelamento:valorFromQuery
  })

  function criaropcaoCredito(){
    params.credito.push(infcreditos)
    alert("Pagamento efetuado com sucesso!")
    console.log(params.credito)
  }

  const infqrcode = reactive({
    valor:"",
    qrcode:""
  })

  function criaropcaoQrcode(){
    params.qrcode.push(infqrcode)
    alert("Pagamento efetuado com sucesso!")
    console.log(params.qrcode)
  }

</script>



<template>


<div class="fundoPag">

<h2 class="tituloPagamento"> Finalize sua compra </h2>



  <p class="ajustePagamento">Escolha seu meio de pagamento</p>
  
  

   <div class="divPagamento">

    <button class="botaoPagamento ajustexd" v-on:click="alteraOpcaopagamento('credito')"> Credito </button>

    <button class="botaoPagamento ajustelinhaPag1 " v-on:click="alteraOpcaopagamento('qrcode')"> Pix </button>

    </div >

   

    <form v-if="categoria =='credito' " id="infcreditos" v-on:submit.prevent="criaropcaoCredito()">


      <p class="conteudoPagamento"> 

        <label>
        Nome do titular: <input v-model="infcreditos.nome">
        </label>
        
      </p>

      
      <p class="conteudoPagamento">

        <label>
        Numero do cartão: <input v-model="infcreditos.numeroCartao">
        </label>

      </p>


      <p class="conteudoPagamento">

        <label>
          
        CPF do titular cartão: <input v-model="infcreditos.cpf">
        </label>

      </p>


      <p class="conteudoPagamento">

        <label>
        Data de validade: <input placeholder="MM/AA" type="date" v-model="infcreditos.validade">
        </label>

      </p>

      
      <p class="conteudoPagamento">

        <label>
        CVV: <input v-model="infcreditos.codigoSeguranca">
        </label>

      </p>


      <p class="conteudoPagamento">

    <label>
    Valor: <label> {{infcreditos.parcelamento}} </label>
    </label>

  </p>

                    

    <button class="botaoPagamento ajustelinhaPag2"> Finalizar Compra </button> <button class="botaoPagamento ajustelinhaPag2"> Cancelar </button>

    </form>



    <form v-if="categoria =='qrcode'" id="infqrcode" v-on:submit.prevent="criaropcaoQrcode()">

      


        <p class="conteudoPagamento">

          <label>
          <strong> Vencimento </strong>  
          </label>

          <p class="ajustevalid"> Hoje, validação ate as 17:00 </p>


        </p>

      <p class="conteudoPagamento">

      <label>
      QR Code: 
      </label>
      <div>
      <img v-if="route.query.tipo === 'doctor'" class="qrtamanho" src="/public/qrdoctor.jpg">
      <img v-else class="qrtamanho" src="/public/qrclinica.jpg">
      </div>
      </p>


      
    
    <button class="botaoPagamento ajustelinhaPag3 ajustecimapag3"> Finalizar Compra </button> <button class="botaoPagamento ajustelinhaPag3"> Cancelar </button>
   




    </form>
</div>
  
</template>