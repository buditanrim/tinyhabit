<script setup>
import { ref } from 'vue'

let isActive = ref(true)

</script>

<template>
  <main>
    <div 
      class="h-5 w-5 block bg-sky-500 border" 
      :class="{ 'active' : isActive }"
      @click="isActive = !isActive" 
    >
      a
    </div>
  </main>
</template>

<style>

.active {
background: green;
}

</style>