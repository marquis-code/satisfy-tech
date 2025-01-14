<!-- components/TheNavbar.vue -->
<template>
    <nav  :class="[shade === 'default' ? 'bg-white' : 'from-blue-300 to-blue-600 w-full']" class="w-full px-4 py-4">
      <div class="container mx-auto">
        <div class="flex items-center justify-between">
          <!-- Logo and Brand -->
          <button class="flex block items-center space-x-2">
            <img src="@/assets/icons/black-logo.svg" />
          </button>
  
          <!-- Navigation Links -->
          <div class="hidden md:flex items-center z-20 space-x-8">
            <NuxtLink 
              v-for="link in navigationLinks" 
              :key="link.name"
              :to="link.href"
              class="text-[#222222] bg-gray-50 text-sm rounded-full px-6 py-2.5 font-semibold hover:text-[#222222] z-20 transition-colors duration-200"
              :class="{ 'font-medium': link.name === 'Projects' }"
            >
              {{ link.name }}
            </NuxtLink>
            <a
              href="#contact-us"
              class="px-4 py-2 bg-gray-50 text-sm text-[#222222] rounded-full font-semibold transition-colors duration-200"
            >
              Contact us
            </a>
          </div>
  
          <!-- Mobile Menu Button -->
          <button 
            class="md:hidden p-2 rounded-lg z-50"
            @click="isMenuOpen = !isMenuOpen"
          >
            <span class="sr-only">Open menu</span>
            <svg
              class="w-6 h-6"
              fill="none"
              stroke="currentColor"
              viewBox="0 0 24 24"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M4 6h16M4 12h16M4 18h16"
              />
            </svg>
          </button>
        </div>
      </div>
  
      <!-- Mobile Menu -->
      <div v-if="isMenuOpen" class="lg:hidden" role="dialog" aria-modal="true">
          <div class="fixed inset-0 z-50"></div>
          <div
            class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
            <div class="flex items-center justify-between">
              <a href="#" class="-m-1.5 p-1.5">
                <span class="sr-only">Your Company</span>
                <img class="h-8 w-auto" src="@/assets/icons/black-logo.svg" alt="">
              </a>
              <button @click="isMenuOpen = !isMenuOpen" type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700">
                <span class="sr-only">Close menu</span>
                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none"
                  stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                  <line x1="18" y1="6" x2="6" y2="18"></line>
                  <line x1="6" y1="6" x2="18" y2="18"></line>
                </svg>
              </button>
            </div>
            <div class="mt-6 flow-root">
              <div class="-my-6 divide-y divide-gray-500/10">
                <div class="space-y-2 py-6">
                  <NuxtLink v-for="(item, idx) in navigationLinks" :key="idx" :to="item.href"
                    class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">
                    {{ item.name }}</NuxtLink>
                </div>
              </div>
            </div>
          </div>
        </div>
    </nav>
  </template>
  
  <script setup lang="ts">
  const isMenuOpen = ref(false)

  const props = defineProps({
    shade: {
      type: String,
      defaultt: 'default'
    }
  })
  
  const navigationLinks = [
    { name: 'Home', href: '/' },
    { name: 'Services', href: '/services' },
    { name: 'Projects', href: '/projects' },
    // { name: 'Contact Us', href: 'contact-us' }
  ]
  </script>

<style scoped>
.router-link-exact-active {
  background-color: #222222;
  color: white;
  border-radius: 35px;
  padding: 10px;
}
</style>