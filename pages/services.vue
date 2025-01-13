<template>
    <main>
        <div class="min-h-screen bg-gradient-to-b from-sky-400 via-blue-500 to-blue-600">
    <nav class="container mx-auto px-4 py-6">
      <div class="flex justify-between items-center">
        <div class="flex items-center">
          <div class="w-8 h-8 bg-blue-600 rounded-lg"></div>
          <span class="ml-2 text-2xl font-bold text-white">Buildr</span>
        </div>
        
        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-8">
          <a href="#" class="text-white hover:text-blue-100">Home</a>
          <a href="#" class="px-4 py-2 bg-black text-white rounded-full">Services</a>
          <a href="#" class="text-white hover:text-blue-100">Projects</a>
          <a href="#" class="text-white hover:text-blue-100">Contact us</a>
        </div>

        <!-- Mobile Menu Button -->
        <button class="md:hidden text-white" @click="toggleMobile">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
          </svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div v-if="isMobileMenuOpen" class="md:hidden mt-4">
        <div class="flex flex-col space-y-4">
          <a href="#" class="text-white hover:text-blue-100">Home</a>
          <a href="#" class="text-white hover:text-blue-100">Services</a>
          <a href="#" class="text-white hover:text-blue-100">Projects</a>
          <a href="#" class="text-white hover:text-blue-100">Contact us</a>
        </div>
      </div>
    </nav>

    <div class="container mx-auto px-4 pt-20 md:pt-32">
      <h1 class="text-4xl md:text-6xl text-white text-center font-bold leading-tight">
        Your Vision 
        <span class="inline-block mx-2 text-red-500 transform translate-y-[-4px]">+</span> 
        our expertise 
        <span class="inline-block mx-2 text-red-500 transform translate-y-[-4px]">=</span>
        <div class="relative inline-block">
          <span class="relative z-10">unmatched results</span>
          <div class="absolute inset-0 w-full">
            <svg class="w-full h-full" viewBox="0 0 300 60">
              <path 
                class="animate-draw" 
                d="M10,30 Q150,60 290,30" 
                fill="none" 
                stroke="#FFD700" 
                stroke-width="2"
              />
            </svg>
          </div>
        </div>
      </h1>
    </div>
  </div>
        <Services />
        <WorkApproachSection />
    </main>
</template>

<script setup lang="ts">
const isMobileMenuOpen = ref(false)

const toggleMobile = () => {
  isMobileMenuOpen.value = !isMobileMenuOpen.value
}
</script>

<style scoped>
.animate-draw {
  stroke-dasharray: 1000;
  stroke-dashoffset: 1000;
  animation: draw 2s ease-in-out forwards;
}

@keyframes draw {
  to {
    stroke-dashoffset: 0;
  }
}
</style>