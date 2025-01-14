<!-- components/MarqueeBanner.vue -->
<template>
    <div class="relative w-full bg-[#F7F7F7] overflow-hidden py-6 mt-20">
      <div class="track flex whitespace-nowrap">
        <!-- Original content -->
        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[#222222] font-medium text-xl">• the future</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Scale with confidence</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Your growth-driven</span>
          <span class="text-red-600 font-medium text-xl">■</span>
        </div>
        <!-- Duplicate content -->
        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[#222222] font-medium text-xl">• the future</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Scale with confidence</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Your growth-driven</span>
          <span class="text-red-600 font-medium text-xl">■</span>
        </div>
        <!-- Additional duplicate for seamless loop -->
        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[#222222] font-medium text-xl">• the future</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Scale with confidence</span>
          <span class="text-red-600 font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-xl">Your growth-driven</span>
          <span class="text-red-600 font-medium text-xl">■</span>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .track {
    animation: scroll 30s linear infinite;
  }
  
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-33.33%);
    }
  }
  
  /* Performance optimizations */
  .track {
    will-change: transform;
    transform: translate3d(0, 0, 0);
  }
  
  /* Optional: Add pause on hover */
  .track:hover {
    animation-play-state: paused;
  }
  </style>
  
  <script setup lang="ts">
  import { onMounted, onUnmounted } from 'vue'
  
  onMounted(() => {
    const checkWidth = () => {
      const track = document.querySelector('.track') as HTMLElement
      const content = track?.firstElementChild as HTMLElement
      
      if (track && content) {
        // Ensure we have enough copies to cover the screen
        const trackWidth = track.offsetWidth
        const contentWidth = content.offsetWidth
        const numCopies = Math.ceil((trackWidth * 2) / contentWidth)
        
        // Add or remove copies as needed
        while (track.children.length < numCopies) {
          track.appendChild(content.cloneNode(true))
        }
      }
    }
  
    // Initial check and window resize listener
    checkWidth()
    window.addEventListener('resize', checkWidth)
  
    onUnmounted(() => {
      window.removeEventListener('resize', checkWidth)
    })
  })
  </script>