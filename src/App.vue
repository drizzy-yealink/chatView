<script setup lang="ts">
import TopBar from './components/TopBar.vue'
import IntputArea from './components/InputArea.vue'
</script>

<template>

  <div >
    <div>
      <TopBar></TopBar>
    </div>
      <IntputArea></IntputArea>
    

  </div>

</template>

<style scoped>
.chat{
  width: 50%;
  
  border: 0.1rem solid red;
}

</style>
