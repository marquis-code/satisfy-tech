<!-- 
<template>
    <div class="relative w-full overflow-hidden py-6 m">
      <div class="track flex whitespace-nowrap">

        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[##EA4335] font-medium text-2xl mx-6">Engineer the future</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[##EA4335] font-medium leading-loose text-2xl">Scale with confidence</span>
          <span class="text-[#EA4335] font-medium text-2xl">■</span>
          <span class="text-[##EA4335] font-medium leading-loose text-2xl">Your growth-driven partner</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
        </div>

        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[##EA4335] font-medium text-2xl mx-6">Engineer the future</span>
          <span class="text-[#EA4335] font-medium text-2xl">■</span>
          <span class="text-[##EA4335] font-medium text-2xl">Scale with confidence</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[##EA4335] font-medium text-2xl">Your growth-driven partner</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
        </div>

        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[##EA4335] font-medium text-2xl mx-6">Engineer the future</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[##EA4335] font-medium leading-loose text-2xl">Scale with confidence</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[##EA4335] font-medium leading-loose text-2xl">Your growth-driven partner</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
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
  </script> -->

  <template>
    <div class="relative w-full overflow-hidden py-6">
      <div class="track flex whitespace-nowrap">
        <!-- Original content -->
        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[#222222] font-medium text-2xl pl-4">Engineer the future</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-2xl">Scale with confidence</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-2xl">Your growth-driven partner</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
        </div>
        <!-- Duplicate content -->
        <div class="flex items-center space-x-6 min-w-max">
          <span class="text-[#222222] font-medium text-2xl pl-4">Engineer the future</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-2xl">Scale with confidence</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
          <span class="text-[#222222] font-medium text-2xl">Your growth-driven partner</span>
          <span class="text-[#EA4335] font-medium text-xl">■</span>
        </div>
      </div>
    </div>
  </template>
  
  <style scoped>
  .track {
    animation: scroll 15s linear infinite; /* Adjust speed */
  }
  
  @keyframes scroll {
    0% {
      transform: translateX(0);
    }
    100% {
      transform: translateX(-50%);
    }
  }
  
  .track {
    will-change: transform;
    transform: translate3d(0, 0, 0);
  }
  
  .track:hover {
    animation-play-state: paused;
  }
  </style>
  
  <script setup lang="ts">
  import { onMounted, onUnmounted } from 'vue';
  
  onMounted(() => {
    const checkWidth = () => {
      const track = document.querySelector('.track') as HTMLElement;
      const content = track?.firstElementChild as HTMLElement;
  
      if (track && content) {
        const trackWidth = track.offsetWidth;
        const contentWidth = content.offsetWidth;
        const numCopies = Math.ceil((trackWidth * 2) / contentWidth);
  
        while (track.children.length < numCopies) {
          track.appendChild(content.cloneNode(true));
        }
  
        // Ensure spacing is maintained between repeated content
        Array.from(track.children).forEach((child: Element) => {
          if (!child.classList.contains('spacer')) {
            const spacer = document.createElement('div');
            spacer.classList.add('spacer');
            spacer.style.width = '1rem';
            track.insertBefore(spacer, child.nextSibling);
          }
        });
      }
    };
  
    checkWidth();
    window.addEventListener('resize', checkWidth);
  
    onUnmounted(() => {
      window.removeEventListener('resize', checkWidth);
    });
  });
  </script>
  