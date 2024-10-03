<script setup>

</script>

<template>


<section>

    <div class="container content">
        
        <img class="medicos" src="/public/medico.jpg"/>
    
        <div>
    
            <div class="row">
            <div class="card xdd">
                <ol class="textopag fonte"> <p><strong><span class="titulo">Bem vindo(a) ao <span class="titulocor2">Portal Saúde+</span></span></strong></p>
                <div>
                <P>Sua jornada para uma mente saudável começa aqui no Portal Saúde+.</P>
                <p>Estamos comprometidos em apoiar sua saúde e promover um estilo de vida ativo e pleno. Navegue, descubra e dê o primeiro passo para transformar sua saúde hoje!</p>
                </div>
                <p class="card2"><strong>Sua saúde é nossa prioridade.</strong></p>


                </ol>
            </div>
        </div>
    
        </div>
    
    </div>
        
    
    
        
    
</section>

<section class="fundonovo">
    
<p class="cortxt">
    Avaliações de nossos <strong> especialistas</strong> sobre como <strong> cuidamos de você</strong>:
    <div class="modalConteudo2">
        <p>Eder Matos</p>
        <p>Especialista em Depressão</p>
        <p>"É um ótimo ponto de partida para quem deseja se informar e encontrar suporte nessa jornada. Cuide de você!"</p>
    </div>
    
    
   
  

    
</p>


</section>
    
   <section>

<!--FONT AWESOME-->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">

<!--GOOGLE FONTS-->
<link rel="preconnect" href="https://fonts.gstatic.com">
<link href="https://fonts.googleapis.com/css2?family=Fredoka+One&family=Play&display=swap" rel="stylesheet"> 

<footer>
<div class="footer">
<div class="row">
<a href="#"><i class="fa fa-facebook"></i></a>
<a href="#"><i class="fa fa-instagram"></i></a>
<a href="#"><i class="fa fa-youtube"></i></a>
<a href="#"><i class="fa fa-twitter"></i></a>
</div>

<div class="row">
<ul>
<li><a href="#">Contate-nos</a></li>
<li><a href="#">Nossos Serviços</a></li>
<li><a href="#">Política de Privacidade</a></li>
<li><a href="#">Termos & Condições</a></li>

</ul>
</div>

<div class="row">
Portal Saúde+ Copyright © 2024 Portal Saúde+ - Todos direitos reservados || Designed By: G.
</div>
</div>
</footer>

   </section>     
    
    

</template>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Sans+Condensed:ital,wght@0,400;1,700&display=swap');

.card {
  border-radius: 10px;
  filter: drop-shadow(0 5px 10px 0 #ffffff);
  width: 800px;
  height: 440px;
  background-color: #ffffff;
  padding: 20px;
  position: relative;
  z-index: 0;
  overflow: hidden;
  transition: 0.6s ease-in;
  margin-top: 20px;
  color: #009c75e3;
}


.card::before {
  content: "";
  position: absolute;
  z-index: -1;
  top: -15px;
  right: -15px;
  background: #07d3a0;
  height:470px;
  width: 25px;
  border-radius: 32px;
  transform: scale(1);
  transform-origin: 80% 80%;
  transition: transform 0.25s ease-out;
}

.card:hover::before{
    transition-delay:0.2s ;

  transform: scale(50);
}

.card:hover{
    color: #ffffff;

}

.card p{
    padding: 10px 0;
}


</style>