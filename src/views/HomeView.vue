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

const habits = ref([])
const newHabitItem = ref('')
const saveItem = () => {
  habits.value.push({id: habits.value.length + 1, label: newHabitItem.value})
  newHabitItem.value =''
}

</script>

<template>
  <main>
    <h1>Tiny Habit</h1>

    <form 
      class="mb-4"
      @submit.prevent="saveItem"
    >
      <input
        v-model="newHabitItem"
        type="text"
        placeholder="Write your habit"
        class="mr-4"
      >
      <button>
        Create a habit
      </button>
    </form>

    <div v-for="habit in habits">
      {{ habit.label }}
    </div>

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
    <p v-if="!habits.length">Start habits to achieve your goal</p>
  </main>
</template>

<style>

.active {
  background: green;
}

</style>