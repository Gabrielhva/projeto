<template>
<div class="divisao">

  <div class="topicos">
    <p>Topicos</p>
    <ul>
      <li>Autismo</li>
      <li>Depressão</li>
      <li>Bipolaridade</li>
      <li>Boderlaine</li>
      <li>Esquizofrenia</li>
      <li></li>
    </ul>

  </div>
  <div>
    <h2>Autismo</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. 
      A, cum asperiores accusantium repellat molestiae fuga expedita 
      dolore, ipsa voluptatum, 
      incidunt non quam blanditiis ab consequuntur architecto magnam
      fugit iure voluptas?</p>
    </div>
  </div>
    
</template>

<style scoped>

ul{
  margin-right: 30px;
  padding: 0;
}

li{
  margin-bottom: 20px;
  background: green;
  color: white;
  padding: 10px;
  text-align: center;
  cursor: pointer;
}
li:hover{
  background: darkgreen;
  transition: 0.3s;
}

.divisao{
  display: flex;
}
.topicos{
  text-align: center;
  width: 800px;
}

</style>