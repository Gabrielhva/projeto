<script setup>

const params = defineProps(["medicos"])

console.log(params)
</script>



<template>

<div> 

<button type="button" class="perfil"> <img src="./imagens/user1.png" class="fotoperfil"></button> 
<p>{{ params.medicos.nome }}</p>
<p>Psicologo</p>

</div>

</template>