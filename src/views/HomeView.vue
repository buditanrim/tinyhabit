<script setup>
import { ref } from 'vue'

const boxes = ref([
  { id: 1, clicked: false },
  { id: 2, clicked: false },
  { id: 3, clicked: false },
  { id: 4, clicked: false },
  { id: 5, clicked: false },
])

function toggleBoxColor(box) {
  box.clicked = !box.clicked;
}

const habit = ref([])

</script>

<template>
  <main>
    <div id="habit-row" class="flex">
      <div class="mr-2">
        <p>Workout</p>
      </div>
      <div class="flex">
        <div
          v-for="box in boxes"
          :key="id"
          class="h-5 w-5 m-0.5 bg-gray-200 border-gray-400"
          :class="{ 'active' : box.clicked }"
          @click="toggleBoxColor(box)"
        >
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