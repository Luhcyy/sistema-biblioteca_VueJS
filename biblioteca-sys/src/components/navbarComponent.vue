<template>
<nav class="navbar navbar-expand-lg navbar-dark custom-bg-dark">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="/">
      <img src="../assets/imgs/CPS_LogotipoMinimoNegativo.png" alt="CPS-icon" class="d-inline-block">
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse justify-content-between" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <router-link class="nav-link navigation-link" aria-current="page" to="/">Inicio</router-link>
        
        <router-link class="nav-link navigation-link" to="/sobre">Sobre</router-link>
      </div>
      <div class="navbar-nav">
        <a class="nav-link text-white" aria-current="page" href="#">Login</a>
        
        <a class="nav-link text-white" href="#">Cadastro</a>
      </div>
    </div>
  </div>
</nav>
</template>


<style scoped>
.custom-bg-dark {
    background-color: #a3130d;
}

.navbar-nav .navigation-link {
    position: relative;
    margin: 0 10px;
    color: white;
}

.navigation-link:active{
    
    color: rgb(231, 216, 216);
}

.navigation-link::after {
    content: '';
    position:absolute;
    left: 0;
    bottom: -9px;
    width: 100%;
    height: 5px;
    background: white;
    transform: scaleX(0);
    transform-origin: right;
    transition: transform .3s;
}

.navigation-link:hover::after {
    transform: scaleX(1);
    transform-origin: left;
}

</style>

