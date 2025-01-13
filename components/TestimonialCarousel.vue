<template>
    <section class="bg-white py-16 px-4 md:px-8">
      <div class="max-w-6xl mx-auto">
        <!-- Header -->
        <div class="text-center mb-16">
          <p class="text-sm uppercase tracking-wider text-gray-600">TESTIMONIALS</p>
          <h2 class="text-3xl md:text-4xl font-semibold text-gray-900 mt-2">
            What our clients are saying
          </h2>
        </div>
  
        <!-- Carousel -->
        <div class="relative max-w-4xl mx-auto">
          <!-- Navigation Buttons -->
          <button 
            @click="prevSlide" 
            class="absolute left-0 top-1/2 -translate-y-1/2 -translate-x-16 bg-[#4F46E5] hover:bg-[#4338CA] text-white rounded-full p-4 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-[#4F46E5]"
            :class="{ 'opacity-50 cursor-not-allowed': currentIndex === 0 }"
            :disabled="currentIndex === 0"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
            </svg>
          </button>
  
          <button 
            @click="nextSlide"
            class="absolute right-0 top-1/2 -translate-y-1/2 translate-x-16 bg-[#4F46E5] hover:bg-[#4338CA] text-white rounded-full p-4 transition-all duration-200 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-[#4F46E5]"
            :class="{ 'opacity-50 cursor-not-allowed': currentIndex === testimonials.length - 1 }"
            :disabled="currentIndex === testimonials.length - 1"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
  
          <!-- Testimonials Container -->
          <div class="overflow-hidden relative bg-[#18181B] rounded-2xl p-10">
            <TransitionGroup 
              name="slide" 
              tag="div" 
              class="relative"
            >
              <div 
                v-for="(testimonial, index) in testimonials" 
                :key="testimonial.id"
                v-show="index === currentIndex"
                class="w-full"
              >
                <!-- Quote Icon -->
                <div class="text-[#4F46E5] mb-6">
                  <!-- <svg width="45" height="36" class="fill-current">
                    <path d="M13.415.043c6.208 0 11.251 4.83 11.251 10.777 0 6.49-5.043 11.32-11.25 11.32-6.209 0-11.252-4.83-11.252-10.777C2.164 4.873 7.206.043 13.415.043zm0 15.607c2.707 0 4.903-2.155 4.903-4.83 0-2.676-2.196-4.83-4.903-4.83-2.707 0-4.904 2.154-4.904 4.83 0 2.675 2.197 4.83 4.904 4.83z"></path>
                  </svg> -->
                  <img src="@/assets/img/quote.png" class="h-6 w-6" />
                </div>
  
                <!-- Testimonial Content -->
                <div class="space-y-8">
                  <p class="text-white text-xl leading-relaxed">{{ testimonial.content }}</p>
                  
                  <!-- Author Info -->
                  <div class="flex items-center space-x-4">
                    <img 
                      :src="testimonial.avatar" 
                      :alt="testimonial.name"
                      class="w-12 h-12 rounded-full object-cover"
                    />
                    <div>
                      <h4 class="text-white font-medium">{{ testimonial.name }}</h4>
                      <p class="text-gray-400">{{ testimonial.title }}</p>
                    </div>
                  </div>
                </div>
              </div>
            </TransitionGroup>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  import quote from '@/assets/img/quote.png'
  import testimonialAvatar from '@/assets/img/testimony-avatar.png'
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
      content: "Buildr transformed our vision into reality, delivering a seamless app that's now essential to our operation. Their team nailed it from strategy to launch.",
      name: "Vivien",
      title: "Co-founder, Grabhub",
      avatar: testimonialAvatar
    },
    {
      id: 2,
      content: "Working with this team has been incredible. They took our complex requirements and delivered a solution that exceeded our expectations.",
      name: "Marcus",
      title: "CTO, TechStart",
      avatar: testimonialAvatar
    },
    {
      id: 3,
      content: "The attention to detail and technical expertise shown by the team was outstanding. They're truly partners in our success.",
      name: "Sarah",
      title: "Product Manager, InnovateCo",
      avatar: testimonialAvatar
    }
  ]);
  
  const currentIndex = ref(0);
  
  const nextSlide = () => {
    if (currentIndex.value < testimonials.value.length - 1) {
      currentIndex.value++;
    }
  };
  
  const prevSlide = () => {
    if (currentIndex.value > 0) {
      currentIndex.value--;
    }
  };
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