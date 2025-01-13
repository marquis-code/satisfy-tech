<template>
    <div class="relative group overflow-hidden rounded-2xl transition-all duration-300 hover:shadow-xl">
      <div class="relative h-[400px] w-full">
        <img 
          :src="study.image" 
          :alt="study.title"
          class=""
        />
        <div class="absolute inset-0 bg-black/50"></div>
        <div class="absolute bottom-0 left-0 p-8 w-full">
          <h3 class="text-2xl font-bold text-white mb-2">{{ study.title }}</h3>
          <p class="text-white/80 text-sm">
            {{ study.categories.join(' / ') }}
          </p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  defineProps<{
    study: CaseStudy;
  }>();
  </script>