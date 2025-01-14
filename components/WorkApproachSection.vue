<template>
    <main class="bg-[#DDDEE6]">
        <section class="py-16 px-4 md:px-8">
            <div class="max-w-6xl mx-auto">
                <!-- Header -->
                <div class="text-center mb-16 space-y-4">
                    <!-- <p
                        class="text-lg md:text-xl text-gray-800 max-w-2xl mx-auto leading-relaxed"
                    >We deliver tailored solutions, seamless collaboration, and unwavering support to bring your vision to life with excellence</p> -->
    
                    <div data-aos="fade-up" class="pt-8">
                        <h6 class="text-sm uppercase tracking-wider text-[#7C7C7C]">our  approach</h6>
                        <h2
                            class="text-2xl md:text-3xl font-medium text-[#EA4335] mt-2"
                        >Seamless Product Lifecycle</h2>
                    </div>
                </div>
    
                <section>
                    <section class="pb-16 px-4 md:px-8">
                        <div class="max-w-6xl mx-auto space-y-32">
                            <!-- Card -->
                            <div
                             data-aos="fade-up"
                                v-for="(reason, idx) in reasonsArray"
                                :key="idx"
                                class="max-w-4xl mx-auto"
                            >
                                <div class="lg:flex space-y-3 lg:space-y-0  gap-20  justify-between ">
                                    <!-- Number and Title -->
                                    <div class="flex gap-3">
                                        <span class="text-[#FF5757] text-sm font-medium">0{{ idx + 1 }}</span>
                                        <h3
                                            class="text-2xl font-medium text-[#161616]"
                                        >{{ reason?.title ?? 'Nil' }}</h3>
                                    </div>
    
                                    <!-- Description -->
                                 <div class="">
                                    <p
                                        class="text-gray-600 text-left leading-relaxed text-[#161616] max-w-xl"
                                    >{{ reason?.content ?? 'Nil' }}</p>
                                 </div>
                                </div>
                            </div>
                        </div>
                    </section>
                </section>
            </div>
        </section>
    </main>
    </template>
      
      <script setup lang="ts">
    const reasonsArray = ref([
  {
    "title": "Discovery & Strategy",
    "content": "Our approach begins with Discovery and strategy, where we work closely with stakeholders to define goals, conduct market research, and develop a strategic product roadmap that aligns with business objectives and user needs."
  },
  {
    "title": "User-Centered Design",
    "content": "In the User-Centered Design phase, we focus on crafting intuitive and visually appealing designs by creating prototypes, mapping user journeys, and refining based on feedback to ensure accessibility and inclusivity."
  },
  {
    "title": "Agile Development",
    "content": "During Agile development, we build scalable and robust software through iterative sprints, ensuring seamless collaboration between teams while leveraging modern tools for efficient deployment and integration."
  },
  {
    "title": "Testing & Validation",
    "content": "We perform manual and automated tests to validate functionality, usability, performance, and security, ensuring the product meets the highest standards before launch."
  },
  {
    "title": "Launch & Deployment",
    "content": "We ensure a smooth launch by preparing a comprehensive go-to-market strategy. From final performance checks to deployment, we handle every detail to ensure the product is delivered seamlessly and is fully optimized for end-users."
  },
  {
    "title": "Collaboration & Communication",
    "content": "Transparency and teamwork are at the core of our approach. We use advanced project management tools and maintain regular updates through meetings and progress reports, ensuring all stakeholders remain informed and aligned throughout the project."
  }
]

    )
    </script>