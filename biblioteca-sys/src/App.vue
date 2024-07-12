<script setup lang="ts">
import { RouterView } from 'vue-router'
import  navbarComponent  from "./components/navbarComponent.vue";
import footerComponent from "./components/footerComponent.vue";

</script>

<template>
<div class="wrapper">
<nav>
  <navbarComponent></navbarComponent>
</nav>

  <main class="content">
    <RouterView />
  </main>

  <footer>
    <footerComponent></footerComponent>
  </footer>
</div>
</template>

<style>

.content{
  flex: 1;
}

.wrapper{
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
</style>

