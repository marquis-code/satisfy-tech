<template>
  <section class="bg-white py-16 px-4 md:px-8">
    <div class="max-w-6xl mx-auto">
      <!-- Header -->
      <div class="text-center mb-16">
        <p class="text-sm uppercase tracking-wider text-[#7C7C7C]">TESTIMONIALS</p>
        <h2 class="text-3xl md:text-4xl font-semibold text-[#222222] mt-2">
          What our clients are saying
        </h2>
      </div>

      <!-- Carousel -->
      <div class="relative max-w-4xl mx-auto">
        <!-- Navigation Buttons for Desktop -->
        <button @click="prevSlide"
          class="absolute left-0 top-1/2 -translate-y-1/2 -translate-x-16 bg-[#4F46E5] hover:bg-[#4338CA] text-white rounded-full p-4 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-[#4F46E5] hidden md:block"
          :class="{ 'opacity-50 cursor-not-allowed': currentIndex === 0 }" :disabled="currentIndex === 0">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
          </svg>
        </button>

        <button @click="nextSlide"
          class="absolute right-0 top-1/2 -translate-y-1/2 translate-x-16 bg-[#4F46E5] hover:bg-[#4338CA] text-white rounded-full p-4 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-[#4F46E5] hidden md:block"
          :class="{ 'opacity-50 cursor-not-allowed': currentIndex === testimonials.length - 1 }"
          :disabled="currentIndex === testimonials.length - 1">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
          </svg>
        </button>

        <!-- Testimonials Container -->
        <div class="overflow-hidden relative bg-[#161616] rounded-2xl py-10 lg:py-0 px-6 lg:p-10">
          <TransitionGroup name="slide" tag="div" class="relative h-[200px]">
            <div
              v-for="(testimonial, index) in testimonials"
              :key="testimonial.id"
              v-show="index === currentIndex"
              class="absolute inset-0 w-full">
              <!-- Quote Icon -->
              <div class="text-[#4F46E5] mb-6">
                <img src="@/assets/img/quote.png" class="h-6 w-6" />
              </div>

              <!-- Testimonial Content -->
              <div class="space-y-4">
                <p class="text-white lg:text-xl leading-relaxed">
                  {{ testimonial.content }}
                </p>

                <!-- Author Info -->
                <div class="flex items-center space-x-4">
                  <img
                    :src="testimonial.avatar"
                    :alt="testimonial.name"
                    class="w-10 h-10 rounded-full object-cover" />
                  <div>
                    <h4 class="text-white font-medium">{{ testimonial.name }}</h4>
                    <p class="text-gray-400 text-sm">{{ testimonial.title }}</p>
                  </div>
                </div>
              </div>
            </div>
          </TransitionGroup>

          <!-- Dot Navigation for Mobile -->
          <div class="flex justify-center mt-20 lg:mt-6 md:hidden">
            <button
              v-for="(testimonial, index) in testimonials"
              :key="testimonial.id"
              @click="goToSlide(index)"
              class="h-3 w-3 rounded-full mx-1 transition-all duration-300"
              :class="currentIndex === index ? 'bg-[#4F46E5]' : 'bg-gray-400'">
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import testimonialAvatar from '@/assets/img/testimony-avatar.png';
import { ref, onMounted, onUnmounted } from 'vue';

interface Testimonial {
  id: number;
  content: string;
  name: string;
  title: string;
  avatar: string;
}

// Sample testimonials data
const testimonials = ref<Testimonial[]>([
  {
    id: 1,
    content:
      "Buildr transformed our vision into reality, delivering a seamless app that's now essential to our operation. Their team nailed it from strategy to launch.",
    name: "Vivien",
    title: "Co-founder, Grabhub",
    avatar: testimonialAvatar,
  },
  {
    id: 2,
    content:
      "Buildr transformed our vision into reality, delivering a seamless app that's now essential to our operation. Their team nailed it from strategy to launch.",
    name: "Vivien",
    title: "Co-founder, Grabhub",
    avatar: testimonialAvatar,
  },
  {
    id: 3,
    content:
      "Buildr's expertise in app development propelled our project from an idea to a fully functional tool that's revolutionizing how we do business. Their approach was straightforward and effective.",
    name: "Winifred",
    title: "Business Developer, Homely",
    avatar: testimonialAvatar,
  },
  {
    id: 4,
    content:
      "Working with Buildr was a game-changer. They took our initial concept and developed a platform that exceeded our expectations, setting us apart in the market..",
    name: "John",
    title: "CEO, Novatoons",
    avatar: testimonialAvatar,
  },
]);

const currentIndex = ref(0);
let interval: ReturnType<typeof setInterval> | null = null;

const nextSlide = () => {
  if (currentIndex.value < testimonials.value.length - 1) {
    currentIndex.value++;
  } else {
    currentIndex.value = 0;
  }
};

const prevSlide = () => {
  if (currentIndex.value > 0) {
    currentIndex.value--;
  } else {
    currentIndex.value = testimonials.value.length - 1;
  }
};

const goToSlide = (index: number) => {
  currentIndex.value = index;
};

const startAutoSlide = () => {
  interval = setInterval(nextSlide, 3000);
};

const stopAutoSlide = () => {
  if (interval) clearInterval(interval);
};

onMounted(() => {
  startAutoSlide();
});

onUnmounted(() => {
  stopAutoSlide();
});
</script>

<style scoped>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.5s ease;
}

.slide-enter-from {
  opacity: 0;
  transform: translateX(100%);
}

.slide-leave-to {
  opacity: 0;
  transform: translateX(-100%);
}

.slide-enter-to,
.slide-leave-from {
  opacity: 1;
  transform: translateX(0);
}
</style>
