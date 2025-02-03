<script setup>

import '~/assets/css/contesuahistoria.css'



</script>

<template>


<h2 class="titulohistoria"> Conte sua Historia </h2>
    <br/><br/>

    <p class="conteudohistoria">
    Compartilhar suas experiências pode criar um senso de conexão com outras pessoas que estão passando por desafios semelhantes.
    Isso pode ajudar os outros a sentir que não estão sozinhos e a encontrar conforto e apoio em histórias semelhantes 
   </p>
   <br/>

   <p class="conteudohistoria"> Preencha os campos abaixo e nos conte sua historia:</p>

   <br/>

    <form > 

        <div class="campohistoria"> 
        <label>
            Nome Completo:
            <br/>
            <input/>

            <br/><br/>

            E-mail:
            <br/>
            <input/>

            <br/><br/>

            Telefone:
            <br/>
            <input/>

            <br/><br/>

            Sua Experiência:
            <br/>
            <textarea rows="10" cols="60" maxlength="500"></textarea>

          
            </label>

            <br/><br/>

         </div>

            <button class="botaohistoria"> Enviar </button>  <button class="botaohistoria"> Cancelar </button>
</form>













</template>