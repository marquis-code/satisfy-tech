<template>
  <main>
    <WhiteNav class="mb-10 z-50" shade="default" />
    <div class="relative isolate overflow-hidden">
      <img
        src="@/assets/img/column.png"
        alt=""
        class="absolute inset-0 -z-10 h-full w-full opacity-40 object-cover"
      />
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl py-32 sm:py-48 lg:py-56">
          <div class="text-center flex justify-center items-center flex-col">
            <h1
              data-aos="fade-up"
              class="text-balance text-5xl font-semibold tracking-tight text-gray-900"
            >
              Build the future of your business
            </h1>
            <p
              class="mt-8 text-pretty flex justify-center items-center lg:max-w-sm text-center text-lg font-light text-gray-500 sm:text-xl/8"
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
    </div>

    <MarqueeBanner />

   <section class="mx-auto w-full max-w-7xl px-4 sm:px-6 lg:px-8 border-4">
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
          class="mt-4 text-center text-[#161616] leading-loose max-w-lg mx-auto text-center"
        >
          <span class="hover:text-green-500 transition-colors duration-300"
            >We
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >turn
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >ambitious
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >ideas
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >into
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >high-performing
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >digital
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >products.
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >Through
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >innovative
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >tech
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >and
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >agile
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >development,
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >we
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >help
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >you
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >move
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >faster,
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >scale
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >smarter,
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >and
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >stay
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >ahead
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >of
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
            >the
          </span>
          <span class="hover:text-green-500 transition-colors duration-300"
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

      <div class="mx-auto max-w-7xl sm:px-2 lg:px-4">
        <div class="mx-auto max-w-2xl px-4 lg:max-w-none">
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
            class="bg-[#444CE7] bg-[#444CE7] text-white px-8 py-3.5 rounded-full font-medium transition-colors duration-300"
          >
            View more
          </NuxtLink>
        </div>
      </div>
    </div>

    <CaseStudies />
    </section>
   <WhyChooseUsSection />
  <section class="mx-auto w-full max-w-7xl px-4 sm:px-6 lg:px-8">
    <TestimonialCarousel />
  </section>

  </main>
</template>

<script setup lang="ts">
const openNav = ref(false);
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
</script>
