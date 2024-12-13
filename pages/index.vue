 <!-- pages/index.vue -->
<template>
<main>
  <div class="min-h-screen bg-gradient-to-br from-white to-sky-50">
    <!-- Navigation -->
    <nav data-aos="fade-up"  class="container mx-auto px-4 py-6">
      <div class="flex items-center justify-between">
        <div class="flex items-center">
          <img src="@/assets/img/loan-logo.png" alt="ClearCredit" class="h-8" />
        </div>
        
        <div class="hidden md:flex items-center space-x-8">
          <a href="#" class="text-sky-400 font-medium">Home</a>
          <a href="#" class="text-gray-600 hover:text-gray-900">Compare Lenders</a>
          <a href="#" class="text-gray-600 hover:text-gray-900">Saving Calculator</a>
          <a href="#" class="text-gray-600 hover:text-gray-900">Blogs</a>
          <a href="#" class="text-gray-600 hover:text-gray-900">Contact Us</a>
        </div>

        <a 
          href="tel:1-844-208-1100" 
          class="bg-sky-400 text-white px-6 py-3 rounded-full hover:bg-sky-500 transition-colors flex items-center"
        >
          <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
          </svg>
          1-844-208-1100
        </a>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-12">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <!-- Left Column -->
        <div class="space-y-8">
          <div>
            <h2 data-aos="fade-up"  class="text-sky-400 text-3xl md:text-4xl font-light mb-4">
              Investment for everyone
            </h2>
            <h1 data-aos="fade-up"  class="text-slate-800 text-4xl md:text-6xl font-bold leading-tight">
              Top Investments,<br />
              All in one place.
            </h1>
          </div>

          <div class="space-y-4">
            <div data-aos="fade-up"  class="flex items-center space-x-2">
              <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Rates from 5.20% - 35.99% APR¹</span>
            </div>
            <div data-aos="fade-up"  class="flex items-center space-x-2">
              <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Loan amounts from $600 to $200,000</span>
            </div>
          </div>

          <div class="space-y-4">
            <div data-aos="fade-up"  class="relative">
              <input 
                type="text" 
                placeholder="Enter amount ($600 - $200,000)" 
                class="w-full px-4 py-3 rounded-lg border border-gray-300 focus:ring-2 focus:ring-sky-400 focus:border-transparent"
              />
              <button class="absolute right-2 top-1 bg-sky-400 text-white px-6 py-2 rounded-lg hover:bg-sky-500 transition-colors">
                Submit
              </button>
            </div>

            <button data-aos="fade-up"  class="w-full bg-sky-100 text-sky-600 px-6 py-4 rounded-lg hover:bg-sky-200 transition-colors flex items-center justify-center space-x-2">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
              <span>Respond to Mail Offer</span>
            </button>
          </div>

          <div data-aos="fade-up"  class="flex items-center space-x-4">
            <div class="flex -space-x-2">
              <img src="@/assets/img/avatar.png" alt="" class="w-8 h-8 rounded-full border-2 border-white" />
              <img src="@/assets/img/avatar.png" alt="" class="w-8 h-8 rounded-full border-2 border-white" />
              <img src="@/assets/img/avatar.png" alt="" class="w-8 h-8 rounded-full border-2 border-white" />
            </div>
            <span class="text-gray-600">50,000+ clients around the world</span>
          </div>
        </div>

        <!-- Right Column -->
        <div data-aos="fade-up"  class="relative ">
          <img 
            src="@/assets/img/loan.png" 
            alt="Woman using phone" 
            class="w-full max-w-lg mx-auto"
          />
        </div>
      </div>
    </main>
  </div>
  <InvestmentOfferings />
  <InvestmentStats />
  <SavingsCalculator />
  <CapitalRaisingSection />
  <!-- <ServicesSection /> -->
  <!-- <CustomerTestimonials /> -->
  <FooterSection />
</main>
</template>

