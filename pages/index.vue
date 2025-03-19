<template>
  <div class="min-h-screen bg-gray-50">
    <WelcomeOverlay />
    <Header />
    <main class="container mx-auto px-4 pb-10">
      <FoodBannerCarousel />
      <PromotedVendors />
      <VendorsInFunaab />
    </main>
  </div>
</template>

<script setup lang="ts">
import Header from '~/components/Header.vue';
import FoodBannerCarousel from '~/components/FoodBannerCarousel.vue';
import PromotedVendors from '~/components/PromotedVendors.vue';
import VendorsInFunaab from '~/components/VendorsInFunaab.vue';
import WelcomeOverlay from '~/components/WelcomeOverlay.vue';
</script>