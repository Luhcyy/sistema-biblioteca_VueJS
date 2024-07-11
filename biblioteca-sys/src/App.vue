<script setup lang="ts">
import { RouterView } from 'vue-router'
import  navbarComponent  from "./components/navbarComponent.vue";
import footerComponent from "./components/footerComponent.vue";

</script>

<template>
<nav>
  <navbarComponent></navbarComponent>
</nav>

  <main>
    
  </main>

  <footer>
    <footerComponent></footerComponent>
  </footer>
  <RouterView />
</template>

<style>
footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>

