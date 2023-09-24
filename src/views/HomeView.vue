<script setup>
import { ref } from 'vue'

let isActive = ref(true)

</script>

<template>
  <main>
    <div class="flex">
      <div class="m-2">
        <p>Workout</p>
      </div>
      <div class="flex">
        <div class="h-5 w-5 m-2 mr-1 bg-gray-200 border-gray-400" :class="{ 'active' : isActive }" @click="isActive = !isActive">
        </div>
        <div class="h-5 w-5 m-2 mr-1 bg-gray-200 border-gray-400" :class="{ 'active' : isActive }" @click="isActive = !isActive">
        </div>
        <div class="h-5 w-5 m-2 mr-1 bg-gray-200 border-gray-400" :class="{ 'active' : isActive }" @click="isActive = !isActive">
        </div>
        <div class="h-5 w-5 m-2 mr-1 bg-gray-200 border-gray-400" :class="{ 'active' : isActive }" @click="isActive = !isActive">
        </div>
        <div class="h-5 w-5 m-2 mr-1 bg-gray-200 border-gray-400" :class="{ 'active' : isActive }" @click="isActive = !isActive">
        </div>
      </div>
    </div>
  </main>
</template>

<style>

.active {
background: green;
}

</style>