<template>
  <main class="flex flex-col min-h-screen font-Roboto bg-gray-baft">
    <RouterView class="shadow-lg"/>
  </main>
</template>

<script setup>
  import { RouterView } from "vue-router"
</script>

<style lang="css" scoped>
  main{
    display: flex;  
    justify-content: center;  
    align-items: center;  
  }

  div {
    background-color: white;
    width: 88vw;
    height: 98vh;
    z-index: 1;
  }

</style>