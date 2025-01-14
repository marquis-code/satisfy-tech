<template>
  <ProductsHeroSection />
    <section class="container mx-auto px-4 py-12">
      <!-- Filter Categories -->
      <div class="flex justify-center items-center flex-wrap gap-4 mb-12">
        <button 
          v-for="category in categories" 
          :key="category"
          @click="activeCategory = category"
          :class="[
            'px-6 py-2 rounded-full text-sm font-medium transition-all',
            activeCategory === category 
              ? 'bg-black text-white' 
              : 'bg-gray-100 text-gray-600 hover:bg-gray-200'
          ]"
        >
          {{ category }}
        </button>
      </div>
  
      <!-- Projects Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <NuxtLink 
          v-for="project in filteredProjects" 
          :key="project.id"
          :to="project.urlPath"
          class="relative block group overflow-hidden rounded-2xl"
        >
          <!-- Project Card -->
          <div class="relative group overflow-hidden rounded-2xl transition-all duration-300 hover:shadow-xl">
      <div class="relative w-full">
        <img 
          :src="project?.image" 
          :alt="project?.title"
          class=""
        />
        <div class="absolute inset-0 bg-black/50"></div>
        <p class="text-white text- font-semibold absolute top-6 left-6 mb-4">{{ project.title }}</p>
        <div class="absolute bottom-0 left-0 p-8 w-full">
          <h3 class="text-lg font-bold text-white mb-2">{{ project?.description }}</h3>
          <p class="text-white/80 text-sm">
            {{ project?.tags.join(' / ') }}
          </p>
        </div>
      </div>
    </div>
        </NuxtLink>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
             import coverDetails1 from '@/assets/img/cover-details1.png'
             import coverDetails2 from '@/assets/img/cover-details2.png'
             import coverDetails3 from '@/assets/img/cover-details3.png'
             import coverDetails4 from '@/assets/img/cover-details4.png'
             import coverDetails5 from '@/assets/img/cover-details5.png'
             import coverDetails6 from '@/assets/img/cover-details6.png'
              import coverDetails7 from '@/assets/img/cover-details7.png'
  interface Project {
    id: number;
    title: string;
    description: string;
    image: string;
    urlPath: string;
    tags: string[];
    categories: string[];
  }
  
  const categories = ref([
    'All',
    'E-Commerce',
    'Real Estate',
    'Artificial Intelligence',
    'Entertainment',
    'Marketplaces'
  ]);
  
  const activeCategory = ref('All');
  
  const projects: Project[] = [
    {
      id: 1,
      title: 'BlackCountry',
      description: 'Simplifying Shared Living in Nigeria',
      image: coverDetails5,
       urlPath: '/projects/black-country',
      tags: ['PropTech', 'Real Estate', 'Social Enterprise'],
      categories: ['Real Estate']
    },
    {
      id: 2,
      title: 'IQly',
      description: 'Revolutionizing Job Searches with an AI-Driven Career Platform',
      image: coverDetails7,
       urlPath: '/projects/iqly',
      tags: ['Career Development', 'EdTech', 'Artificial Intelligence'],
      categories: ['Artificial Intelligence']
    },
    {
      id: 3,
      title: 'Grabhub',
      description: 'Addressing Food Waste with an Innovative Marketplace',
      image: coverDetails6,
      urlPath: '/projects/grabhub',
      tags: ['FoodTech', 'E-Commerce', 'Marketplaces'],
      categories: ['E-Commerce', 'Marketplaces']
    },
    {
      id: 4,
      title: 'Marketsquare',
      description: 'Connecting Local Services with Ease',
      image: coverDetails1,
      urlPath: '/projects/marketsquare',
      tags: ['E-Commerce', 'Marketplaces'],
      categories: ['E-Commerce', 'Marketplaces']
    },
    {
      id: 5,
      title: 'Novatoons',
      description: 'Championing Diverse Narratives: The Novatoons Case Study',
       image: coverDetails2,
       urlPath: '/projects/novatoons',
      tags: ['Entertainment', 'Digital Media'],
      categories: ['Entertainment']
    },
    {
      id: 6,
      title: 'Storipod',
      description: 'Revolutionizing Microblogging for Storytellers',
     image: coverDetails4,
      urlPath: '/projects/storipod',
      tags: ['Entertainment', 'Social Media', 'Digital Media'],
      categories: ['Entertainment']
    }
  ];
  
  const filteredProjects = computed(() => {
    if (activeCategory.value === 'All') {
      return projects;
    }
    return projects.filter(project => 
      project.categories.includes(activeCategory.value)
    );
  });
  </script>