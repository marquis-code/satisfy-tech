<template>
  <main>
    <div class="">
  <header class="absolute inset-x-0 top-0 z-50">
    <nav class="flex items-center justify-between p-6 container mx-auto" aria-label="Global">
      <div class="flex lg:flex-1">
        <a href="#" class="-m-1.5 p-1.5">
          <span class="sr-only">Your Company</span>
          <img class="h-8 w-auto" src="@/assets/icons/white-logo.svg" alt="">
        </a>
      </div>
      <div class="flex lg:hidden">
        <button @click="isMenuOpen = true" type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-400">
          <span class="sr-only">Open main menu</span>
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="3" y1="12" x2="21" y2="12"></line><line x1="3" y1="6" x2="21" y2="6"></line><line x1="3" y1="18" x2="21" y2="18"></line></svg>
        </button>
      </div>
      <div class="hidden lg:flex lg:gap-x-3">
        <!-- {{ router.currentRoute.fullPath }} -->
        <!-- {{ route }} -->
        <NuxtLink to="/" class="text-sm/6 flex justify-center items-center font-semibold bg-black/50 text-white">Home</NuxtLink>
        <NuxtLink to="/services" class="text-sm/6 flex px-5 rounded-full justify-center items-center font-semibold bg-black/50 text-white">Services</NuxtLink>
        <NuxtLink to="/projects" class="text-sm/6 flex px-5 rounded-full justify-center items-center font-semibold bg-black/50 text-white">Projects</NuxtLink>
        <!-- <a href="#contact-us" class="text-sm/6 font-semibold text-white bg-[#444CE7] contact-link">Contact us</a> -->
         <button onclick="document.getElementById('contact-us').scrollIntoView({ behavior: 'smooth' });" class="text-sm/6 flex px-5 rounded-full justify-center items-center font-semibold bg-black/50 text-white">Contact Us</button>
      </div>
      <!-- <div class="hidden lg:flex lg:flex-1 lg:justify-end">
        <a href="#" class="text-sm/6 font-semibold text-white">Log in <span aria-hidden="true">&rarr;</span></a>
      </div> -->
    </nav>
    <!-- Mobile menu, show/hide based on menu open state. -->
    <div v-if="isMenuOpen" class="lg:hidden" role="dialog" aria-modal="true">
      <!-- Background backdrop, show/hide based on slide-over state. -->
      <div class="fixed inset-0 z-50"></div>
      <div class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-gray-900 px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-white/10">
        <div class="flex items-center justify-between">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="h-8 w-auto" src="@/assets/icons/white-logo.svg" alt="">
          </a>
          <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-400">
            <span class="sr-only">Close menu</span>
            <svg class="size-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true" data-slot="icon">
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18 18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
        <div class="mt-6 flow-root">
          <div class="-my-6 divide-y divide-gray-500/25">
            <div class="space-y-2 py-6">
              <NuxtLink to="/" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-white hover:bg-gray-800">Home</NuxtLink>
              <NuxtLink to="/services" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-white hover:bg-gray-800">Services</NuxtLink>
              <NuxtLink to="/projects" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-white hover:bg-gray-800">Projects</NuxtLink>
              <!-- <NuxtLink to="/" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-white hover:bg-gray-800">Contact Us</NuxtLink> -->
            </div>
            <!-- <div class="py-6">
              <a href="#" class="-mx-3 block rounded-lg px-3 py-2.5 text-base/7 font-semibold text-white hover:bg-gray-800">Log in</a>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </header>

  <div class="relative isolate overflow-hidden pt-14">
    <img src="@/assets/img/cta-bg.png" alt="" class="absolute inset-0 -z-10 h-full w-full object-cover">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto py-32 sm:py-48 lg:py-56">
        <div class="text-center">
          <h1 data-aos="fade-up" class="text-balance text-3xl lg:text-7xl font-semibold tracking-tight text-white">Build the future of your business</h1>
          <p data-aos="fade-up" class="-mt-8 text-pretty text-lg font-bold text-white sm:text-xl/8">Your Vision, Our Mission — Together, We’ll Build Exceptional Software</p>
          <div data-aos="fade-up" class="mt-10 flex items-center justify-center gap-x-6">
            <a
                href="#contact-us"
                class="rounded-full bg-[#444CE7] px-6 py-3 text-sm font-semibold text-white shadow-sm focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-[#444CE7]"
              >
                Ready to Build
              </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

    <!-- <WhiteNav class="mb-10 z-50" shade="default" />
    <div class="relative isolate overflow-hidden border-4">
      <img
        src="@/assets/img/hero-section.png"
        alt=""
        class="absolute inset-0 -z-10 h-full w-screen  object-cover"
      />
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl py-32 sm:py-48 lg:py-56">
          <div class="text-center flex justify-center items-center flex-col">
            <h1
              data-aos="fade-up"
              class="text-balance text-5xl font-semibold tracking-tight text-white"
            >
              Build the future of your business
            </h1>
            <p
              class="text-pretty flex justify-center items-center text-center text-lg text-white sm:text-xl/8"
            >
              Your Vision, Our Mission — Together, We’ll Build Exceptional
              Software
            </p>
            <div
              data-aos="fade-up"
              class="mt-10 flex items-center justify-center gap-x-6"
            >
              <a
                href="#contact-us"
                class="rounded-full bg-[#444CE7] px-6 py-3 text-sm font-semibold text-white shadow-sm focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-[#444CE7]"
              >
                Ready to Build
              </a>
            </div>
          </div>
        </div>
      </div>
    </div> -->

    <MarqueeBanner />

   <section class="mx-auto container px-6">
    <div class="bg-white">
      <div
        data-aos="fade-up"
        class="max-w-3xl px-6 lg:px-0 mx-auto flex-col items-center flex justify-center items-center w-full mt-20"
      >
        <h2
          class="text-3xl text-center font-bold tracking-tight text-[#161616]"
        >
          Innovation That Accelerates Your Growth
        </h2>
        <p
          class="mt-4 text-center text-semibold text-[#161616] text-lg leading-loose max-w-lg mx-auto text-center"
        >
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >We
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >turn
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >ambitious
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >ideas
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >into
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >high-performing
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >digital
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >products.
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >Through
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >innovative
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >tech
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >and
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >agile
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >development,
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >we
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >help
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >you
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >move
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >faster,
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >scale
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >smarter,
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >and
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >stay
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >ahead
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >of
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >the
          </span>
          <span class="hover:text-[#444CE7] transition-colors duration-300"
            >competition.
          </span>
        </p>
      </div>

      <div
        data-aos="fade-up"
        class="max-w-3xl mx-auto flex-col items-center flex justify-center items-center w-full mt-20"
      >
        <p
          class="mt-4 text-[#7C7C7C] leading-loose max-w-lg mx-auto text-center"
        >
          OUR SERVICES
        </p>
        <h2 class="text-3xl font-bold tracking-tight text-[#161616]">
          What we offer
        </h2>
      </div>

      <div class="">
        <div class="">
          <div class="mt-16 grid grid-cols-1 gap-x-6 gap-y-6 lg:grid-cols-3">
            <div
              data-aos="fade-up"
              v-for="(item, idx) in offerings"
              :key="idx"
              class="sm:flex rounded-xl p-6 bg-gray-25 rounded-lg lg:block"
            >
              <div class="sm:shrink-0">
                <img class="size-14" src="@/assets/icons/service.svg" alt="" />
              </div>
              <div class="mt-4 sm:ml-6 sm:mt-0 lg:ml-0 lg:mt-6">
                <h3 class="text-lg font-bold text-gray-900">
                  {{ item.title ?? "Nil" }}
                </h3>
                <p class="mt-2 leading-snug text-[#222222]">
                  {{ item.desc }}
                </p>
              </div>
            </div>
          </div>
        </div>

        <div class="text-center mt-20">
          <NuxtLink
            to="/services"
            class="bg-[#444CE7] hover:bg-[#3A40C9] transition text-white px-8 py-3.5 rounded-full font-medium transition-colors duration-300"
          >
            View more
          </NuxtLink>
        </div>
      </div>
    </div>

    <CaseStudies />
    </section>
   <WhyChooseUsSection />
  <section class="mx-auto container px-6 pb-44">
    <TestimonialCarousel />
  </section>

  </main>
</template>

<script setup lang="ts">
const openNav = ref(false);
const route = useRoute()
const router = useRouter()
const offerings = ref([
  {
    title: "Custom software development",
    desc: `We follow a meticulous product management process to create
                  innovative solutions that address the specific needs of our users. From ideation to launch, we
                  prioritize user research, design thinking, and agile development to build products that make a
                  difference.`,
  },
  {
    title: "UI/UX design and product strategy",
    desc: `We understand the importance of a seamless user experience, where
                  we focuses on creating user-friendly navigation, engaging UX/UI design, and optimizing conversions
                  through relevant content and consistent branding.`,
  },
  {
    title: "Cloud & infrastructure consulting",
    desc: `We offer cutting-edge software development services that drive
                  business growth and innovation. Our team of experts specializes in creating robust web and mobile
                  applications tailored to meet the unique needs of your business`,
  },
]);

const isMenuOpen = ref(false);
</script>

<style scoped>
.router-link-exact-active {
  background-color: #444CE7; /* Matches the blue color */
  color: white; /* White text */
  border-radius: 20px; /* Rounded edges */
  font-weight: bold; /* Ensures the text is bold */
  padding: 8px 20px;
}
</style>