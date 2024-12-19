<template>
    <section class="min-h-screen bg-[#F8FAFC] flex items-center justify-center p-4 md:p-8">
      <div class="max-w-7xl w-full flex flex-col md:flex-row items-center justify-between p-8 md:p-16 gap-8">
        <!-- Left Content -->
        <div class="flex-1 max-w-md">
          <h1 data-aos="fade-up"  class="text-[#1F2937] text-4xl md:text-5xl font-bold leading-tight mb-6">
            Start investing with ease
          </h1>
          <p data-aos="fade-up"  class="text-[#6B7280] text-lg mb-8 leading-relaxed">
            We’re dedicated to transforming your financial 
aspirations into realities, offering expert 
solutions with a commitment to trust.

          </p>
          <button data-aos="fade-up"  class="bg-[#2F855A] hover:bg-[#276749] text-white px-8 py-3 rounded-md font-medium transition-colors duration-200">
            Lets Talk
          </button>
        </div>
  
        <!-- Right Illustration -->
        <div class="flex-1 relative">
          <!-- Background Pattern -->
          <div class="absolute top-0 right-0 w-48 h-48 bg-[#E5E7EB] opacity-20 rounded-full blur-3xl"></div>
          
          <!-- Investment Growth Illustration -->
          <div class="relative z-10">
            <div class="relative w-full max-w-md mx-auto">
              <!-- Plant and Growth Elements -->
              <div class="relative">
                <!-- Coins Stack -->
                <div class="absolute bottom-0 left-1/4 w-16 h-20 bg-[#F3F4F6] rounded-lg"></div>
                <div class="absolute bottom-8 left-1/3 w-16 h-24 bg-[#F3F4F6] rounded-lg"></div>
                
                <!-- Growth Chart Icon -->
                <div class="absolute top-4 right-8 bg-white rounded-full p-2 shadow-md">
                  <svg class="w-6 h-6 text-[#2F855A]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path strokeLinecap="round" strokeLinejoin="round" strokeWidth="2" d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6"></path>
                  </svg>
                </div>
  
                <!-- Character -->
                <div  class="relative z-20">
                  <img data-aos="fade-up"  src="@/assets/img/cuate.png" alt="Investor illustration" class="w-full max-w-xs mx-auto"/>
                </div>
  
                <!-- Plant -->
                <div class="absolute bottom-0 right-1/4 w-24 h-48">
                  <div class="absolute bottom-0 w-2 h-32 bg-[#2F855A] rounded-full"></div>
                  <div class="absolute bottom-24 left-1/2 transform -translate-x-1/2 w-4 h-4 bg-[#E74694] rounded-full"></div>
                  <div class="absolute bottom-16 -left-4 w-8 h-12 bg-[#2F855A] rounded-full transform -rotate-45"></div>
                  <div class="absolute bottom-24 -right-4 w-8 h-12 bg-[#2F855A] rounded-full transform rotate-45"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  // No additional logic needed for this component
  </script>