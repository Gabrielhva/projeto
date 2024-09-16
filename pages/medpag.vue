<script setup>


const params = defineProps(["medicos"]);

</script>




<template>


<section class="fundo">

<h1>Especialistas</h1>

<div class="flex_container">

    
    <Medicos v-bind:medicos="medicos[0]"/>
    <Medicos v-bind:medicos="medicos[1]"/>
    <Medicos v-bind:medicos="medicos[2]"/>
    <Medicos v-bind:medicos="medicos[3]"/>
    <Medicos v-bind:medicos="medicos[4]"/>
    <Medicos v-bind:medicos="medicos[5]"/>

    
    
   </div>

</section>


</template>