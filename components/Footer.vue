<template>
    <section class="bg-[#1C1C1C] text-white py-16 px-4 md:px-8">
      <div class="max-w-7xl mx-auto grid md:grid-cols-2 gap-12">
        <!-- Left Column - Contact Info -->
        <div class="bg-[#1D1D1D]">
          <h2 class="text-4xl font-semibold mb-4">Level up your brand</h2>
          <p class="text-gray-400 mb-12">
            We' love to hear from you. Our friendly team is always here to chat.
          </p>
  
          <!-- Contact Methods -->
          <div class="space-y-8">
            <!-- Email -->
            <div class="flex items-start gap-4">
              <div class="text-[#3B82F6] mt-1">
                <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-medium mb-1">Email us</h3>
                <a href="mailto:example@buildr.com" class="text-[#3B82F6] hover:underline">example@buildr.com</a>
              </div>
            </div>
  
            <!-- Office -->
            <div class="flex items-start gap-4">
              <div class="text-[#3B82F6] mt-1">
                <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-medium mb-1">Office</h3>
                <p class="text-[#3B82F6]">100 Smith Street</p>
                <p class="text-[#3B82F6]">Collingwood VIC 3066 AU</p>
              </div>
            </div>
  
            <!-- Phone -->
            <div class="flex items-start gap-4">
              <div class="text-[#3B82F6] mt-1">
                <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
              </div>
              <div>
                <h3 class="text-lg font-medium mb-1">Phone</h3>
                <p class="text-[#3B82F6]">+1 (555) 000-0000</p>
              </div>
            </div>
          </div>
  
          <!-- Social Links -->
          <div class="flex gap-4 mt-12">
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24">
                <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
              </svg>
            </a>
          </div>
        </div>
  
        <!-- Right Column - Contact Form -->
        <form @submit.prevent="handleSubmit" class="space-y-6 b">
          <div class="grid md:grid-cols-2 gap-6">
            <div>
              <label class="block text-sm font-medium mb-2">First name</label>
              <input
                v-model="form.firstName"
                type="text"
                class="w-full px-4 py-3 bg-[#2C2C2C] rounded-lg focus:ring-2 focus:ring-blue-500 outline-none"
                placeholder="First name"
              >
            </div>
            <div>
              <label class="block text-sm font-medium mb-2">Last name</label>
              <input
                v-model="form.lastName"
                type="text"
                class="w-full px-4 py-3 bg-[#2C2C2C] rounded-lg focus:ring-2 focus:ring-blue-500 outline-none"
                placeholder="Last name"
              >
            </div>
          </div>
  
          <div>
            <label class="block text-sm font-medium mb-2">Email</label>
            <input
              v-model="form.email"
              type="email"
              class="w-full px-4 py-3 bg-[#2C2C2C] rounded-lg focus:ring-2 focus:ring-blue-500 outline-none"
              placeholder="you@company.com"
            >
          </div>
  
          <div>
            <label class="block text-sm font-medium mb-2">Phone number</label>
            <div class="flex">
              <select
                v-model="form.countryCode"
                class="px-3 py-3 bg-[#2C2C2C] rounded-l-lg border-r border-gray-600 focus:ring-2 focus:ring-blue-500 outline-none"
              >
                <option value="+1">+1</option>
                <option value="+44">+44</option>
                <option value="+61">+61</option>
              </select>
              <input
                v-model="form.phone"
                type="tel"
                class="flex-1 px-4 py-3 bg-[#2C2C2C] rounded-r-lg focus:ring-2 focus:ring-blue-500 outline-none"
                placeholder="+1 (000) 000-0000"
              >
            </div>
          </div>
  
          <div>
            <label class="block text-sm font-medium mb-2">Message</label>
            <textarea
              v-model="form.message"
              rows="4"
              class="w-full px-4 py-3 bg-[#2C2C2C] rounded-lg focus:ring-2 focus:ring-blue-500 outline-none"
              placeholder="Enter a message..."
            ></textarea>
          </div>
  
          <div class="flex items-center">
            <input
              v-model="form.privacyPolicy"
              type="checkbox"
              class="w-4 h-4 bg-[#2C2C2C] rounded border-gray-600 text-blue-500 focus:ring-blue-500"
            >
            <label class="ml-2 text-sm text-gray-400">
              You agree to our privacy policy.
            </label>
          </div>
  
          <button
            type="submit"
            class="w-full bg-[#3B82F6] text-white py-3 px-6 rounded-lg hover:bg-blue-600 transition-colors focus:ring-2 focus:ring-offset-2 focus:ring-blue-500"
          >
            Send message
          </button>
        </form>
      </div>
  
      <!-- Footer -->
      <div class="max-w-7xl mx-auto mt-16 pt-8 border-t border-gray-800 flex justify-between items-center">
        <a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a>
        <p class="text-gray-400">© 2023 Buildr</p>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  const form = ref({
    firstName: '',
    lastName: '',
    email: '',
    countryCode: '+1',
    phone: '',
    message: '',
    privacyPolicy: false
  });
  
  const handleSubmit = () => {
    // Add your form submission logic here
    console.log('Form submitted:', form.value);
  };
  </script>