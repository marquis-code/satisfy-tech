<template>
  <section class="py-16 px-4 max-w-7xl mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-sm uppercase tracking-wider text-[#7C7C7C]">PROJECTS</h2>
      <h1 class="text-3xl font-bold text-[#222222]">Case Study</h1>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
     <NuxtLink v-for="(item, idx) in caseStudies" :key="idx"  :to="item.urlPath">
      <img :src="item.image" class="" />
     </NuxtLink>
      <!-- <CaseStudyCard
        v-for="study in caseStudies"
        :key="study.id"
        :title="study.title"
        :urlPath="study.urlPath"
        :image="study.image"
        :categories="study.categories"
        :studyObj="study"
      /> -->
    </div>

    <div class="text-center mt-20">
      <NuxtLink to="/projects" class="bg-[#444CE7] bg-[#444CE7] text-white px-8 py-3.5 rounded-full font-medium transition-colors duration-300">
        View more
      </NuxtLink>
    </div>
  </section>
</template>

<script setup lang="ts">
import caseStudy1 from '@/assets/img/case-study1.png'
import caseStudy2 from '@/assets/img/case-study2.png'
import caseStudy3 from '@/assets/img/case-study3.png'
import caseStudy4 from '@/assets/img/case-study4.png'
const caseStudies = ref([
  {
    id: '1',
    title: 'Simplifying Shared Living in Nigeriassss',
    urlPath: '/projects/black-country',
    image: caseStudy1,
    categories: ['PropTech', 'Real Estate', 'Social Enterprise']
  },
  {
    id: '2',
    title: 'Revolutionizing Job Searches with an AI-Driven Career Platform',
    urlPath: '/projects/iqly',
    subtitle: 'Career Development / EdTech / Artificial Intelligence',
    image: caseStudy2,
    categories: ['Career Development', 'EdTech', 'Artificial Intelligence']
  },
  {
    id: '3',
    title: 'Addressing Food Waste with an Innovative Marketplace',
    urlPath: '/projects/grabhub',
    subtitle: 'FoodTech / E-Commerce / Marketplaces',
    image: caseStudy3,
    categories: ['FoodTech', 'E-Commerce', 'Marketplaces']
  },
  {
    id: '4',
    title: 'Connecting Local Services with Ease',
    urlPath: '/projects/marketsquare',
    subtitle: 'E-Commerce / Marketplaces',
    image: caseStudy4,
    categories: ['E-Commerce', 'Marketplaces']
  }
])
</script>