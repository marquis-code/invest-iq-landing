<template>
    <div class="min-h-screen bg-[#F0F9FF] relative overflow-hidden">
      <!-- Background Decorative Elements -->
      <div class="absolute top-0 left-0 w-[400px] h-[400px] bg-[#BAE6FD] rounded-full opacity-20 blur-3xl -translate-x-1/2 -translate-y-1/2"></div>
      <div class="absolute bottom-0 right-0 w-[600px] h-[600px] bg-[#BAE6FD] rounded-full opacity-20 blur-3xl translate-x-1/3 translate-y-1/3"></div>
  
      <div class="max-w-6xl mx-auto px-4 py-16 relative z-10">
        <h1 class="text-[#1E293B] text-4xl md:text-5xl font-bold mb-12">Our services</h1>
  
        <div class="bg-white rounded-3xl shadow-lg p-6 md:p-10">
          <div class="space-y-8">
            <ServiceItem
              v-for="(service, index) in services"
              :key="service.title"
              :number="String(index + 1).padStart(2, '0')"
              :title="service.title"
              :description="service.description"
            />
          </div>
        </div>
  
        <!-- FAQ Section -->
        <div class="mt-12 text-center">
          <button class="text-[#0EA5E9] text-xl font-semibold hover:text-[#0369A1] transition-colors">
            FAQ
          </button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
    const props = defineProps({
      number: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      }
    })

  
  const services = ref([
    {
      title: "Your Information",
      description: "We'll ask you a few questions to better understand your financial situation and preferences. This helps us narrow down your lender and rate eligibility. What you receive are real rates, not mere estimates."
    },
    {
      title: "Compare Rates",
      description: "We'll ask you a few questions to better understand your financial situation and preferences. This helps us narrow down your lender and rate eligibility. What you receive are real rates, not mere estimates."
    },
    {
      title: "Close Your Loan and Fund Your Goal",
      description: "We'll ask you a few questions to better understand your financial situation and preferences. This helps us narrow down your lender and rate eligibility. What you receive are real rates, not mere estimates."
    },
    {
      title: "Sign Your Documents",
      description: "We'll ask you a few questions to better understand your financial situation and preferences. This helps us narrow down your lender and rate eligibility. What you receive are real rates, not mere estimates."
    },
    {
      title: "Funds on Their Way",
      description: "We'll ask you a few questions to better understand your financial situation and preferences. This helps us narrow down your lender and rate eligibility. What you receive are real rates, not mere estimates."
    }
  ])

  </script>
  
  <style scoped>
  .group:last-child {
    border-bottom: none;
    padding-bottom: 0;
  }
  </style>