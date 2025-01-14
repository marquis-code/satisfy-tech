<template>
    <div class="group block relative overflow-hidden rounded-2xl">
      <div class="aspect-w-16 aspect-h-9 w-full relative">
        <!-- <img :src="image" :alt="title" class="" /> -->
        <!-- <div class="absolute hidden  inset-0 bg-black/60 flex flex-col justify-end p-6">
          <h3 class="text-white hidden text-l font-semibold mb-2">{{ title }}</h3>
          <p class="text- font-bold hidden text-white absolute top-6 left-6">{{name}}</p>
          <div class="flex gap-2 mb-3">
            <span v-for="tag in tags" :key="tag" 
              class="text-xs text-white/80 border-r border-white/20 pr-2 last:border-0">
              {{ tag }}
            </span>
          </div>
        </div> -->
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  const props = defineProps({
    image: {
      type: String
    },
    title: {
      type: String
    },
    href: {
      type: String
    },
    name: {
      type: String
    },
    tags: {
      type: Array
    }
  })
  </script>
  