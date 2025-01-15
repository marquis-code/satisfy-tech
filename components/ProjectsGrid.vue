<template>
  <ProductsHeroSection  />
    <section class="mx-auto w-full max-w-7xl px-4 sm:px-6 lg:px-8 py-12">
      <!-- Filter Categories -->
      <div class="flex justify-center items-center flex-wrap gap-4 mb-12 z-10">
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
        <CaseStudyCard
        v-for="project in filteredProjects" 
        :key="project.id"
        :title="project.title"
        :urlPath="project.urlPath"
        :image="project.image"
        :categories="project.categories"
        :studyObj="project"
      />
        <!-- <NuxtLink 
          v-for="project in filteredProjects" 
          :key="project.id"
          :to="project.urlPath"
          class="relative block group overflow-hidden rounded-2xl"
        >

          <div class="relative group overflow-hidden rounded-2xl transition-all duration-300 hover:shadow-xl">
      <div class="relative w-full">
        <img 
          :src="project?.image" 
          :alt="project?.title"
          class=""
        />
        <div class="absolute inset-0 bg-black/50"></div>
        <p class="text-white text-xl font-semibold absolute top-6 left-6 mb-4">{{ project.title }}</p>
        <div class="absolute bottom-0 left-0 p-8 w-full">
          <h3 class="text-2xl font-bold text-white mb-2">{{ project?.description }}</h3>

        </div>
      </div>
    </div>
        </NuxtLink> -->
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  import storipod from '@/assets/img/covers/storipod.png'
  import blackcountry from '@/assets/img/covers/blackcountry.png'
  import iqly from '@/assets/img/covers/iqly.png'
  import marketsquare from '@/assets/img/covers/marketsquare.png'
  import novatoons from '@/assets/img/covers/novatoons.png'
  import grabhub from '@/assets/img/covers/grabhub.png'
  interface Project {
    id: number;
    title: string;
    name: string;
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
      name: 'BlackCountry',
      title: 'Simplifying Shared Living in Nigeria',
      image: blackcountry,
       urlPath: '/projects/black-country',
      tags: ['PropTech', 'Real Estate', 'Social Enterprise'],
      categories: ['Real Estate']
    },
    {
      id: 2,
      name: 'IQly',
      title: 'Revolutionizing Job Searches with an AI-Driven Career Platform',
      image: iqly,
       urlPath: '/projects/iqly',
      tags: ['Career Development', 'EdTech', 'Artificial Intelligence'],
      categories: ['Artificial Intelligence']
    },
    {
      id: 3,
      name: 'Grabhub',
      title: 'Addressing Food Waste with an Innovative Marketplace',
      image: grabhub,
      urlPath: '/projects/grabhub',
      tags: ['FoodTech', 'E-Commerce', 'Marketplaces'],
      categories: ['E-Commerce', 'Marketplaces']
    },
    {
      id: 4,
      name: 'Marketsquare',
      title: 'Connecting Local Services with Ease',
      image: marketsquare,
      urlPath: '/projects/marketsquare',
      tags: ['E-Commerce', 'Marketplaces'],
      categories: ['E-Commerce', 'Marketplaces']
    },
    {
      id: 5,
      name: 'Novatoons',
      title: 'Championing Diverse Narratives: The Novatoons Case Study',
       image: novatoons,
       urlPath: '/projects/novatoons',
      tags: ['Entertainment', 'Digital Media'],
      categories: ['Entertainment']
    },
    {
      id: 6,
      name: 'Storipod',
      title: 'Revolutionizing Microblogging for Storytellers',
     image: storipod,
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