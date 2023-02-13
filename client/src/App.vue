<template>
  <main class="font-Roboto bg-gray-baft">
    <RouterView class="shadow-lg"/>
  </main>
</template>

<script setup>
  import { RouterView } from "vue-router"
</script>

<style lang="css" scoped>
  main{
    width: 100vw;
    display: flex;  
    justify-content: center;  
    align-items: center;  
  }

  div {
    background-color: white;
    width: 90vw;
    height: inherit;
    z-index: 1;
    overflow: hidden;
  }

</style>