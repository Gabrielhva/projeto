<script setup>


const params = defineProps(["medicos"]);

</script>




<template>


<section class="fundo">

<h1>Especialistas</h1>

<div class="flex_container">

    
    <Medicos  v-bind:medicos="medicos"/>
    
    
    
   </div>

</section>


</template>