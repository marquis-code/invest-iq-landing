<template>
    <section class="bg-[#E8F1EC] py-24">
      <div class="container mx-auto px-4">
        <div class="flex flex-col lg:flex-row items-center gap-12">
          <div class="lg:w-1/2 space-y-6">
            <h2 class="text-4xl lg:text-5xl font-bold text-gray-800 leading-tight">
              Our newsletter are not just good; they're legendary
            </h2>
            <p class="text-lg text-gray-600">
              But hey, don't take our word for it—join the ranks of over 400k subscribers who swear by the greatness of Tomi from Trove. Subscribe now and see what all the hype is about!
            </p>
            <form @submit.prevent="handleSubmit" class="space-y-4 max-w-md">
              <input 
                type="text" 
                placeholder="Full Name"
                class="w-full px-4 py-3 rounded-md border border-gray-300 focus:border-gray-500 focus:ring-1 focus:ring-gray-500"
              />
              <input 
                type="email" 
                placeholder="Email Address"
                class="w-full px-4 py-3 rounded-md border border-gray-300 focus:border-gray-500 focus:ring-1 focus:ring-gray-500"
              />
              <button 
                type="submit"
                class="w-full bg-black text-white py-3 rounded-md hover:bg-gray-800 transition-colors"
              >
                Subscribe
              </button>
            </form>
          </div>
          <div class="lg:w-1/2">
            <div class="relative">
              <!-- Tweet Cards -->
              <div class="space-y-4">
                <div class="bg-black text-white p-4 rounded-xl shadow-lg">
                  <div class="flex items-center gap-3 mb-2">
                    <div class="w-10 h-10 rounded-full bg-gray-600"></div>
                    <div>
                      <p class="font-semibold">Username</p>
                      <p class="text-gray-400 text-sm">@handle</p>
                    </div>
                  </div>
                  <p class="text-gray-200">Your mails are unique and different. For a corporate finance mail, it almost sounds like I am gossiping with a friend when reading your mail.</p>
                </div>
                <!-- Add more tweet cards as needed -->
              </div>
              <!-- Navigation Dots -->
              <div class="flex justify-center mt-6 gap-2">
                <button class="w-2 h-2 rounded-full bg-gray-300"></button>
                <button class="w-2 h-2 rounded-full bg-gray-500"></button>
                <button class="w-2 h-2 rounded-full bg-gray-300"></button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  const handleSubmit = () => {
    // Handle form submission
    console.log('Form submitted')
  }
  </script>