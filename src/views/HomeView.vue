<script setup>
</script>

<template>
  <main>
    <div 
      class="h-5 w-5 bg-sky-500" 
      :class="{ 'active' : isActive }"
      @click="isActive = !isActive" ></div>
  </main>
</template>
