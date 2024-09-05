


<script>
  export default {
    data() {
      return {
        topicos: [
          'Autismo',
          'Bipolaridade',
          'Bordelaine',
          'Depressão',
          'Esquizofrenia',
          'Transtorno de estresse pós-traumático',
          'Transtorno Obsessivo-Compulsivo'
        ],
        dependencias: [
          'Dependência alcoólica',
          'Dependência de Drogas Ilícitas',
          'Dependência de Medicamentos'
        ]
      };
    },
    methods: {
      handleClick(item) {
      /* handclick Essa função será executada sempre que um botão for clicado. 
      A função recebe um parâmetro event , que representa o evento 
      de clique. Isso permite que a função saiba qual elemento foi 
      clicado e obtenha informações sobre esse evento */
        alert(`Você clicou em: ${item}`);
      }
    }
  };
  </script>

<template>
    <div>
      <h2>Tópicos</h2>
      <div class="button-container">
        <div v-for="topico in topicos" :key="topico">
          <button @click="handleClick(topico)">{{ topico }}</button>
        </div>
      </div>
  
      <h2>Dependências</h2>
      <div class="button-container">
        <div v-for="dependencia in dependencias" :key="dependencia">
          <button @click="handleClick(dependencia)">{{ dependencia }}</button>
        </div>
      </div>
    </div>

    <NuxtLink to="/">voltar</NuxtLink>
  </template>
  
  
  
  <style scoped>
  .button-container {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
  }
  
  button {
    padding: 10px;
    background-color: #006400; /* Verde escuro */
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  </style>

  
  