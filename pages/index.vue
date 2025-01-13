<template>
  <main>
      <div class="bg-white">
<header class="absolute inset-x-0 top-0 z-50">
  <nav class="flex items-center justify-between p-6 lg:px-8" aria-label="Global">
    <div class="flex lg:flex-1">
      <a href="#" class="-m-1.5 p-1.5">
        <span class="sr-only">Your Company</span>
        <img class="h-8 w-auto" src="@/assets/img/logo-content.png" alt="">
      </a>
    </div>
    <div class="flex lg:hidden">
      <button @click="openNav = true" type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700">
        <span class="sr-only">Open main menu</span>
        <!-- <svg class="size-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon">
          <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
        </svg> -->
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg>
      </button>
    </div>
    <div class="hidden lg:flex lg:gap-x-12">
      <NuxtLink to="/" class="text-sm/6 font-semibold text-gray-900">Home</NuxtLink>
      <NuxtLink to="/services" class="text-sm/6 font-semibold text-gray-900">Services</NuxtLink>
      <NuxtLink to="/projects" class="text-sm/6 font-semibold text-gray-900">Projects</NuxtLink>
      <NuxtLink to="/" class="text-sm/6 font-semibold text-gray-900">Contact Us</NuxtLink>
    </div>
    <div class="hidden lg:flex lg:flex-1 lg:justify-end">
      <a href="#" class="text-sm/6 font-semibold text-gray-900">Log in <span aria-hidden="true">&rarr;</span></a>
    </div>
  </nav>
  <!-- Mobile menu, show/hide based on menu open state. -->
  <div v-if="openNav" class="lg:hidden" role="dialog" aria-modal="true">
    <!-- Background backdrop, show/hide based on slide-over state. -->
    <div class="fixed inset-0 z-50"></div>
    <div class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
      <div class="flex items-center justify-between">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">Your Company</span>
          <img class="h-8 w-auto" src="=@/assets/img/logo-content.png" alt="">
        </a>
        <button @click="openNav = false" type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700">
          <span class="sr-only">Close menu</span>
          <!-- <svg class="size-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon">
            <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
          </svg> -->
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="18" y1="6" x2="6" y2="18"></line><line x1="6" y1="6" x2="18" y2="18"></line></svg>
        </button>
      </div>
      <div class="mt-6 flow-root">
        <div class="-my-6 divide-y divide-gray-500/10">
          <div class="space-y-2 py-6">
            <NuxtLink to="/" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">Home</NuxtLink>
            <NuxtLink to="/services" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">Services</NuxtLink>
            <NuxtLink to="/projects" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">Projects</NuxtLink>
            <NuxtLink to="/" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">Contect Us</NuxtLink>
          </div>
          <div class="py-6">
            <NuxtLink to="/" class="-mx-3 block rounded-lg px-3 py-2.5 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">Log in</NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</header>

<div class="relative isolate pt-14">
  <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
    <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"></div>
  </div>
  <div class="py-24 sm:py-32 lg:pb-40">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl text-center">
        <h1 class="text-balance text-5xl font-semibold tracking-tight text-gray-900 sm:text-7xl">Build the future of your business</h1>
        <p class="mt-8 text-pretty text-lg font-medium text-gray-500 sm:text-xl/8">Your Vision, Our Mission — Together, We’ll Build Exceptional Software</p>
        <div class="mt-10 flex items-center justify-center gap-x-6">
          <a href="#" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Ready to Build</a>
        </div>
      </div>
      <div class="mt-16 flow-root sm:mt-24">
        <div class="-m-2 p-2 ring-inset lg:-m-4 lg:p-4">
          <img src="@/assets/img/puzzle.png" alt="App screenshot" width="2432" height="1442" class="rounded-md ring-gray-900/10">
        </div>
      </div>
    </div>
  </div>
  <div class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
    <div class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"></div>
  </div>
</div>
</div>



<div class="bg-white">
<div class="mx-auto max-w-7xl py-24 sm:px-2 sm:py-32 lg:px-4">
  <div class="mx-auto max-w-2xl px-4 lg:max-w-none">
    <div class="max-w-3xl">
      <h2 class="text-4xl font-bold tracking-tight text-gray-900">Innovation That Accelerates Your Growth</h2>
      <p class="mt-4 text-gray-500">We turn ambitious ideas into high-performing digital products. Through innovative tech and agile development, we help you move faster, scale smarter, and stay ahead of the competition.</p>
    </div>
    <div class="mt-16 grid grid-cols-1 gap-x-8 gap-y-10 lg:grid-cols-3">
      <div class="sm:flex lg:block">
        <div class="sm:shrink-0">
          <img class="size-16" src="@/assets/icons/service.svg" alt="">
        </div>
        <div class="mt-4 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
          <h3 class="text-sm font-medium text-gray-900">Custom software development</h3>
          <p class="mt-2 text-sm text-gray-500">We follow a meticulous product management process to create innovative solutions that address the specific needs of our users. From ideation to launch, we prioritize user research, design thinking, and agile development to build products that make a difference.</p>
        </div>
      </div>
      <div class="sm:flex lg:block">
        <div class="sm:shrink-0">
          <img class="size-16" src="@/assets/icons/service.svg" alt="">
        </div>
        <div class="mt-4 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
          <h3 class="text-sm font-medium text-gray-900">UI/UX design and product strategy</h3>
          <p class="mt-2 text-sm text-gray-500">We understand the importance of a seamless user experience, where we focuses on creating user-friendly navigation, engaging UX/UI design, and optimizing conversions through relevant content and consistent branding.</p>
        </div>
      </div>
      <div class="sm:flex lg:block">
        <div class="sm:shrink-0">
          <img class="size-16" src="@/assets/icons/service.svg" alt="">
        </div>
        <div class="mt-4 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
          <h3 class="text-sm font-medium text-gray-900">Cloud & infrastructure consulting</h3>
          <p class="mt-2 text-sm text-gray-500">We offer cutting-edge software development services that drive business growth and innovation. Our team of experts specializes in creating robust web and mobile applications tailored to meet the unique needs of your business</p>
        </div>
      </div>
    </div>
  </div>
</div>
</div>


<CaseStudies />


<WhyChooseUsSection />


<TestimonialCarousel />

<Foooter />

  </main>
</template>

<script setup lang="ts">
const openNav = ref(false)
</script>