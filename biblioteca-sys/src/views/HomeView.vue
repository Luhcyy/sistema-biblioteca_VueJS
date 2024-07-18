<script setup lang="ts">

</script>

<template>
  <section class="custom-container">
        <img src="../assets/imgs/fundo-branco.jpg" alt="Slide 1" class="background-image">

        <div class="container mt-2 mb-0">

          <div class="row">
            <div class=" col-sm-12 col-md-6 image-container">
              <img src="../assets/imgs/reading-vector.png" alt="">
            </div>

            <div class="col content-container">

              <div class="welcome-container">
        <h1 class="main-title">Biblioteca Fatec Araras</h1>
        <h5 class="sub-title">Tenha acesso a todos os livros disponiveis no colégio e saiba o momento certo para buscar o seu!</h5>

        
      </div>

              <div class="logo-container">
          <img src="../assets/imgs/cps-logo.png" alt="" class="cps-logo">
          <img src="../assets/imgs/fatec-araras_logo-transparent.png" alt="" class="fatec-logo">
          
              </div>

              <router-link class="search-btn" to="/catalogo">Procurar livros <img src="../assets/imgs/book-bookmark-solid.svg" alt="" class="bookmark-icon"></router-link>
      </div>
      </div>
      </div>
  </section>
</template>

<style scoped>
.custom-container {
  position: relative;
  width: 100%;
  min-height: calc(100vh - 100px);  
  overflow: auto;
  
}

.custom2 {
  display: flex;
  flex-direction: column;
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
  z-index: -11;
}

.custom-container .image-container {
    display: flex;
    justify-content: center;
    align-items: center;
    
}

.image-container img {
    height: 500px;
    width: 500px;
}

.custom-container .content-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.logo-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center; 
}

.custom-container .cps-logo {
  width: 240px; 
  height: 220px;
  margin-top: -50px;
  margin-bottom: -50px;
  margin-left: -70px;
}

.custom-container .fatec-logo {
  width: 180px; 
  height: 240px;
  margin-top: -50px;
  margin-bottom: -50px;
}

.welcome-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.custom-container .main-title {
  text-align: center;
  font-weight: 700;
  color: #a3130d; 
  font-weight: 700;
}

.custom-container .sub-title {
  text-align: center; 
  font-weight: 500;
}

.custom-container .search-btn {
  display: flex;
  width: 300.001px;
  height: 69.994px;
  background-color: #475d68;
  border-style: none;
  border-radius: 6px;
  color: white;
  font-size: 24.998px;
  font-weight: 500;
  justify-content: center;
  align-items: center;
  text-decoration: none;
  box-shadow: 0 0.4rem 1rem -0.75rem hsla(0, 0%, 0%, 0.25);
  margin-top: 40px;
}

.custom-container .search-btn:hover {
  background-color: #5c7480;
}

.search-btn .bookmark-icon {
  height: 29.997px;
  width: 29.997px;
  margin-left: 9.999px;
}

@media only screen and (max-width: 1000px) {
  .image-container img {
    display: none;
  }

  .image-container { 
    display: none;
  }

  .content-container {
    margin-top: 80px;
  }

 
}

</style>
