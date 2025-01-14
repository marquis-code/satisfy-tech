<template>
  <main>
    <div class="bg-white">
      <WhiteNav shade="defa" />
      <div class="relative isolate pt-14">
        <div class="">
          <div class="mx-auto max-w-7xl px-6 lg:px-8">
            <div class="mx-auto max-w-2xl text-center">
              <h1 data-aos="fade-up" class="text-balance text-5xl font-semibold tracking-tight text-gray-900">Build the future
                of your business</h1>
            <div data-aos="fade-up" class="flex justify-center items-center -mt-10">
              <p class="mt-8 text-pretty lg:max-w-sm text-center text-lg font-light text-gray-500 sm:text-xl/8">Your Vision, Our Mission —
                Together, We’ll Build Exceptional Software</p>
            </div>
              <div data-aos="fade-up" class="mt-10 flex items-center justify-center gap-x-6">
                <a href="#contact-us"
                  class="rounded-full bg-[#444CE7] px-6 py-3 text-sm font-semibold text-white shadow-sm focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-[#444CE7]">Ready
                  to Build</a>
              </div>
            </div>
            <div class="mt-16 flow-root sm:mt-24">
              <div data-aos="fade-up" class="-m-2 p-2 ring-inset lg:-m-4 lg:p-4 flex justify-center items-center">
                <img data-aos="fade-up" src="@/assets/img/puzzle.png" alt="App screenshot" width="800" height="800"
                  class="rounded-md ring-gray-900/10">
              </div>
            </div>
          </div>
        </div>
        <div
          class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]"
          aria-hidden="true">
          <div
            class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]"
            style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)">
          </div>
        </div>
      </div>
    </div>

    <MarqueeBanner />



    <div class="bg-white">
      <div data-aos="fade-up" class="max-w-3xl px-6 lg:px-0 mx-auto flex-col items-center flex justify-center items-center w-full mt-20">
            <h2 class="text-3xl text-center font-bold tracking-tight text-[#161616]">Innovation That Accelerates Your Growth</h2>
            <p class="mt-4 text-center text-[#161616] leading-loose max-w-lg mx-auto text-center">We turn ambitious ideas into high-performing digital products. Through
              innovative tech and agile development, we help you move faster, scale smarter, and stay ahead of the
              competition.</p>
          </div>


          <div data-aos="fade-up" class="max-w-3xl  mx-auto flex-col items-center flex justify-center items-center w-full mt-20">
            <p class="mt-4 text-[#7C7C7C] leading-loose max-w-lg mx-auto text-center">OUR SERVICES</p>
            <h2 class="text-3xl font-bold tracking-tight text-[#161616]">What we offer</h2>
          </div>


      <div class="mx-auto max-w-7xl sm:px-2 lg:px-4">
        <div class="mx-auto max-w-2xl px-4 lg:max-w-none ">
          <div class="mt-16 grid grid-cols-1 gap-x-6 gap-y-6 lg:grid-cols-3">
            <div data-aos="fade-up" v-for="(item, idx) in offerings" :key="idx" class="sm:flex rounded-xl p-6 bg-gray-25 rounded-lg lg:block">
              <div class="sm:shrink-0">
                <img class="size-14" src="@/assets/icons/service.svg" alt="">
              </div>
              <div class="mt-4 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
                <h3 class="text-lg font-bold text-gray-900">{{ item.title ?? 'Nil' }}</h3>
                <p class="mt-2 lg:text-sm leading-loose text-[#222222]">{{ item.desc }}</p>
              </div>
            </div>
          </div>
        </div>

        <div class="text-center mt-20">
      <NuxtLink to="/services" class="bg-[#444CE7] bg-[#444CE7] text-white px-8 py-3.5 rounded-full font-medium transition-colors duration-300">
        View more
      </NuxtLink>
    </div>
      </div>
    </div>


    <CaseStudies />


    <WhyChooseUsSection />


    <TestimonialCarousel />

    <!-- <Footer /> -->

  </main>
</template>

<script setup lang="ts">
const openNav = ref(false)
const offerings = ref([
  {
    title: 'Custom software development',
    desc: `We follow a meticulous product management process to create
                  innovative solutions that address the specific needs of our users. From ideation to launch, we
                  prioritize user research, design thinking, and agile development to build products that make a
                  difference.`
  },
  {
    title: 'UI/UX design and product strategy',
    desc: `We understand the importance of a seamless user experience, where
                  we focuses on creating user-friendly navigation, engaging UX/UI design, and optimizing conversions
                  through relevant content and consistent branding.`
  },
  {
    title: 'Cloud & infrastructure consulting',
    desc: `We offer cutting-edge software development services that drive
                  business growth and innovation. Our team of experts specializes in creating robust web and mobile
                  applications tailored to meet the unique needs of your business`
  }
])
</script>