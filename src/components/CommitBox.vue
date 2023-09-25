<template>
    <div
      class="h-5 w-5 m-0.5 bg-gray-200 border-gray-400"
      :class="{ 'active': isActive }"
      @click="toggleActive">
      {{ label }}
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    props: ['id', 'label'],
    setup(props) {
      const isActive = ref(false);
  
      const toggleActive = () => {
        isActive.value = !isActive.value;
      };
  
      return {
        isActive,
        toggleActive,
      };
    },
  };
  </script>