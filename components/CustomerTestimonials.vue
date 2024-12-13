<template>
    <section class="py-16 px-4 max-w-6xl mx-auto">
      <!-- Header -->
      <div class="text-center mb-12">
        <h2 class="text-[#1E293B] text-4xl md:text-5xl font-bold mb-4">Our customers says</h2>
        <p class="text-[#64748B] text-lg max-w-2xl mx-auto">
          Make your life easier with comprehensive integration support that allows financial planning to be more seamless.
        </p>
      </div>
  
      <!-- Testimonials Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- First Testimonial -->
        <div class="flex flex-col md:flex-row gap-6 items-start">
          <img 
            src="@/assets/img/test1.png" 
            alt="Freeda Richards" 
            class="w-full md:w-64 h-64 object-cover rounded-lg"
          />
          <div class="bg-[#F0F9FF] p-6 rounded-lg flex-1 relative">
            <div class="absolute top-6 right-6 text-[#BAE6FD] text-6xl font-serif">"</div>
            <h3 class="text-[#1E293B] text-2xl font-bold mb-4 relative z-10">
              I have been using this service for the past year
            </h3>
            <p class="text-[#64748B] mb-4">
              Their team is extremely knowledgeable and always goes above and beyond to help me achieve my goals.
            </p>
            <div>
              <h4 class="text-[#1E293B] font-semibold">Freeda Richards</h4>
              <p class="text-[#64748B]">3 years of using Raizze</p>
            </div>
          </div>
        </div>
  
        <!-- Second Testimonial -->
        <div class="flex flex-col md:flex-row-reverse gap-6 items-start">
          <img 
          src="@/assets/img/test2.png" 
            alt="Andrea Piacquadio" 
            class="w-full md:w-64 h-64 object-cover rounded-lg"
          />
          <div class="bg-[#FFF7ED] p-6 rounded-lg flex-1 relative">
            <div class="absolute top-6 right-6 text-[#FECACA] text-6xl font-serif">"</div>
            <h3 class="text-[#1E293B] text-2xl font-bold mb-4 relative z-10">
              I was hesitant to invest in the stock market
            </h3>
            <p class="text-[#64748B] mb-4">
              They provided me with the education and resources I needed to make informed decisions.
            </p>
            <div>
              <h4 class="text-[#1E293B] font-semibold">Andrea Piacquadio</h4>
              <p class="text-[#64748B]">First years of using Raizze</p>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Action Buttons -->
      <div class="flex flex-col sm:flex-row items-center justify-center gap-4 mt-12">
        <button class="bg-[#F97316] hover:bg-[#EA580C] text-white px-8 py-3 rounded-full font-medium transition-colors">
          Get Started
        </button>
        <button class="text-[#1E293B] hover:text-[#0F172A] border-2 border-[#E2E8F0] px-8 py-3 rounded-full font-medium transition-colors">
          Watch videos
        </button>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  // No additional logic needed for this component
  </script>
  
  <style scoped>
  /* Custom quotation mark styling */
  .font-serif {
    font-family: Georgia, serif;
  }
  </style>