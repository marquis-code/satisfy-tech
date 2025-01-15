<template>
    <div class="flex justify-center items-center">
      <img
        v-if="currentImage === 1"
        class="h-60 transition-opacity duration-500"
        src="@/assets/img/first-iteration.png"
        alt="First Iteration"
      />
      <img
        v-if="currentImage === 2"
        class="h-60 transition-opacity duration-500"
        src="@/assets/img/second-iteration.png"
        alt="Second Iteration"
      />
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, onMounted, onUnmounted } from "vue";
  
  const currentImage = ref(1); // Keeps track of the current image
  let intervalId: NodeJS.Timeout;
  
  onMounted(() => {
    intervalId = setInterval(() => {
      // Switch between images 1 and 2
      currentImage.value = currentImage.value === 1 ? 2 : 1;
    }, 3000); // Change image every 3 seconds
  });
  
  onUnmounted(() => {
    // Clear the interval when the component is unmounted
    clearInterval(intervalId);
  });
  </script>
  
  <style scoped>
  /* Add styles if necessary */
  </style>
  