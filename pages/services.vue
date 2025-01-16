<template>
  <main>
    <div class="bg-gradient-to-b to-[#444CE7] via-[#824DF8] from-[#26D1FF] pb-32">
      <WhiteNav shade="coloured" />
      <div class="mx-auto w-full max-w-7xl px-4 z-0 sm:px-6 lg:px-8 pt-20 flex justify-center items-center">
        <TextSwitch />

        <!-- <img class="h-96" src="@/assets/img/first-iteration.png" />
      <img class="h-96" src="@/assets/img/second-iteration.png" /> -->

        <!-- <h1 class="text-4xl md:text-6xl text-white text-center font-bold leading-tight">
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
      </h1> -->
      </div>
    </div>

    <!-- <p data-aos="fade-up" class="max-w-2xl mx-auto font-medium text-xl px-3 lg:px-0 text-center text-[#222222] leading-loose pt-16">
    Our services are designed to turn your ideas into products. From strategic management to seamless design, robust development, precise and quality assurance, we bring expertise and passion to every project
  </p> -->
    <p data-aos="fade-up"
      class="max-w-2xl mx-auto font-medium text-xl px-3 z-0 lg:px-0 text-center text-[#222222] leading-loose pt-16">
      <span class="hover:text-yellow-400 transition-colors duration-300">Our </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">services </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">are </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">designed </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">to </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">turn </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">your </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">ideas </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">into </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">products. </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">From </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">strategic </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">management </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">to </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">seamless </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">design, </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">robust </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">development, </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">precise </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">and </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">quality </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">assurance, </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">we </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">bring </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">expertise </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">and </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">passion </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">to </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">every </span>
      <span class="hover:text-yellow-400 transition-colors duration-300">project. </span>
    </p>

    <div data-aos="fade-up"
      class="max-w-3xl  mx-auto flex-col items-center flex justify-center items-center w-full mt-20">
      <p class="mt-4 text-[#7C7C7C] leading-loose max-w-lg mx-auto text-center">OUR SERVICES</p>
      <h2 class="text-3xl font-bold tracking-tight text-[#161616]">What we offer</h2>
    </div>

    <section class="mx-auto w-full max-w-7xl ">
      <ServicesSection />
    </section>
    <WorkApproachSection class="mt-16" />
    <section class="mx-auto w-full max-w-7xl ">
      <StackCloud />
    </section>
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



<style scoped>
.router-link-exact-active {
  background-color: '#222222';
  color: white;
  border-radius: 35px;
  padding: 10px;
}
</style>