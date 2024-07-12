<script setup lang="ts">

</script>

<template>
  <section class="custom-container">
        <img src="../assets/imgs/fundo-branco.jpg" alt="Slide 1" class="background-image">
        <img src="../assets/imgs/reading-vector.png" alt="" class="overlay-image">
        
        <img src="../assets/imgs/cps-logo.png" alt="" class="cps-logo">
        <img src="../assets/imgs/fatec-araras_logo-transparent.png" alt="" class="fatec-logo">

        <h1 class="main-title">Biblioteca Fatec Araras</h1>
        <h5 class="sub-title">Tenha acesso a todos os livros disponiveis no colégio e saiba o momento certo para buscar o seu!</h5>

        <button class="search-btn">Buscar livros <img src="../assets/imgs/book-bookmark-solid.svg" alt="" class="bookmark-icon"></button>
  </section>
</template>

<style scoped>
.custom-container {
  position: relative;
  width: 100%;
  height: 525px;
  overflow: hidden;
}

.custom-container .background-image {
  display: block;
  position: absolute;
  width: 100%;
  max-height: 400px;
  object-fit:fill;
  transform: scaleY(-1) scaleX(-1);
  top: -150px;
  clip-path: inset(50px 0 0 0);
  opacity: 0.20;
}

.custom-container .overlay-image {
  position: absolute;
  top: -4.392vw; 
  left: -2.928vw; 
  width: 49.78vw; 
  height: 49.78vw; 
}


.custom-container .cps-logo {
  position: absolute;
  top: -3.66vw; 
  left: 43.145vw; 
  width: 27.086vw; 
  height: 21.23vw; 
}

.custom-container .fatec-logo {
  position: absolute;
  top: -3.10vw; 
  left: 75.403vw; 
  width: 20.498vw; 
  height: 21.23vw; 
}

.custom-container .main-title {
  position: absolute;
  top: 16.837vw; 
  left: 57.467vw; 
  width: 36.603vw; 
  height: 21.23vw;
  font-size: 2.709vw;
  font-weight: 700;
  color: #a3130d; 
}

.custom-container .sub-title {
  position: absolute;
  text-align: center;
  top: 21.962vw; 
  left: 53.807vw; 
  width: 36.603vw; 
  height: 21.23vw; 
  font-size: 1.464vw;
}

.custom-container .search-btn {
  position: absolute;
  top: 29.283vw; 
  left: 60.029vw; 
  width: 21.962vw;
  height: 5.124vw;
  background-color: #475d68;
  border-style: none;
  border-radius: 10px;
  color: white;
  font-size: 1.83vw;
  font-weight: 500;
  justify-content: center;
  align-items: center;
  box-shadow: 0 0.4rem 1rem -0.75rem hsla(0, 0%, 0%, 0.25);
}

.custom-container .search-btn:hover {
  background-color: #5c7480;
}

.search-btn .bookmark-icon {
  height: 2.196vw;
  width: 2.196vw;
  margin-left: 0.732vw;
}

</style>
