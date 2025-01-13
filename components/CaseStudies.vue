<template>
  <section class="py-16 px-4 max-w-7xl mx-auto">
    <div class="text-center mb-12">
      <h2 class="text-sm uppercase tracking-wider text-gray-600 mb-4">PROJECTS</h2>
      <h1 class="text-4xl font-bold text-gray-900">Case Study</h1>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <CaseStudyCard
        v-for="study in caseStudies"
        :key="study.id"
        :study="study"
      />
    </div>

    <div class="text-center mt-12">
      <button class="bg-blue-600 hover:bg-blue-700 text-white px-8 py-3 rounded-full font-medium transition-colors duration-300">
        View more
      </button>
    </div>
  </section>
</template>

<script setup lang="ts">
import caseStudy1 from '@/assets/img/case-study1.png'
import caseStudy2 from '@/assets/img/case-study2.png'
import caseStudy3 from '@/assets/img/case-study3.png'
import caseStudy4 from '@/assets/img/case-study4.png'
const caseStudies: CaseStudy[] = [
  {
    id: '1',
    title: 'Simplifying Shared Living in Nigeria',
    image: caseStudy1,
    categories: ['PropTech', 'Real Estate', 'Social Enterprise']
  },
  {
    id: '2',
    title: 'Revolutionizing Job Searches with an AI-Driven Career Platform',
    subtitle: 'Career Development / EdTech / Artificial Intelligence',
    image: caseStudy2,
    categories: ['Career Development', 'EdTech', 'Artificial Intelligence']
  },
  {
    id: '3',
    title: 'Addressing Food Waste with an Innovative Marketplace',
    subtitle: 'FoodTech / E-Commerce / Marketplaces',
    image: caseStudy3,
    categories: ['FoodTech', 'E-Commerce', 'Marketplaces']
  },
  {
    id: '4',
    title: 'Connecting Local Services with Ease',
    subtitle: 'E-Commerce / Marketplaces',
    image: caseStudy4,
    categories: ['E-Commerce', 'Marketplaces']
  }
];
</script>