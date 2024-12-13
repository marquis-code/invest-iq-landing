<!-- components/SavingsCalculator.vue -->
<template>
    <div class="min-h-screen bg-gradient-to-br from-white to-sky-50 relative overflow-hidden">
      <!-- Background Decorative Elements -->
      <div class="absolute -left-64 top-0 w-128 h-128 bg-sky-200 rounded-full opacity-20"></div>
      <div class="absolute -right-32 bottom-0 w-96 h-96 bg-sky-200 rounded-full opacity-20"></div>
  
      <div class="container mx-auto px-4 py-12">
        <!-- Header -->
        <div class="text-center mb-12">
          <h2 data-aos="fade-up"  class="text-sky-400 uppercase tracking-wide text-sm font-medium mb-4">
            Savings Calculator
          </h2>
          <h1 data-aos="fade-up"  class="text-slate-800 text-4xl md:text-5xl font-bold leading-tight">
            Calculate Your Savings with<br />Clear Credit AI
          </h1>
        </div>
  
        <!-- Calculator Card -->
        <div data-aos="fade-up"  class="max-w-3xl mx-auto bg-white rounded-3xl shadow-xl p-8 relative z-10">
          <!-- Current Loan Details -->
          <div class="space-y-6 mb-12">
            <h3 data-aos="fade-up"  class="text-slate-800 text-xl font-semibold">
              1. Enter your current loan details
            </h3>
            
            <div class="grid md:grid-cols-3 gap-4">
              <div data-aos="fade-up"  class="col-span-3 md:col-span-1">
                <label class="block text-sm text-slate-600 mb-1">Loan Amount</label>
                <div class="relative">
                  <input
                    v-model="currentLoan.amount"
                    type="text"
                    class="w-full px-4 py-2 border border-gray-200 rounded-lg focus:ring-2 focus:ring-sky-400 focus:border-transparent"
                    placeholder="Enter amount"
                  />
                  <span class="absolute right-4 top-2 text-slate-400">$</span>
                </div>
              </div>
  
              <div data-aos="fade-up"  class="md:col-span-1">
                <label class="block text-sm text-slate-600 mb-1">Interest Rate</label>
                <div class="relative">
                  <input
                    v-model="currentLoan.rate"
                    type="text"
                    class="w-full px-4 py-2 border border-gray-200 rounded-lg focus:ring-2 focus:ring-sky-400 focus:border-transparent"
                  />
                  <span class="absolute right-4 top-2 text-slate-400">%</span>
                </div>
              </div>
  
              <div data-aos="fade-up"  class="md:col-span-1">
                <label class="block text-sm text-slate-600 mb-1">Loan Term</label>
                <select
                  v-model="currentLoan.term"
                  class="w-full px-4 py-2 border border-gray-200 rounded-lg focus:ring-2 focus:ring-sky-400 focus:border-transparent appearance-none bg-white"
                >
                  <option value="2">2 Years</option>
                  <option value="3">3 Years</option>
                  <option value="5">5 Years</option>
                </select>
              </div>
            </div>
          </div>
  
          <!-- Compare Rate Section -->
          <div data-aos="fade-up"  class="space-y-6 mb-12">
            <h3 class="text-slate-800 text-xl font-semibold">
              2. Choose a rate to compare
            </h3>
            <p class="text-slate-600 text-sm">
              Our lender rates vary from <span class="font-medium">5.20%</span> to <span class="font-medium">35.99%</span> APR
            </p>
  
            <div data-aos="fade-up"  class="grid md:grid-cols-2 gap-4">
              <div class="relative">
                <label class="block text-sm text-slate-600 mb-1">Interest Rate</label>
                <input
                  v-model="newLoan.rate"
                  type="text"
                  class="w-full px-4 py-2 border border-gray-200 rounded-lg focus:ring-2 focus:ring-sky-400 focus:border-transparent"
                />
                <span class="absolute right-4 top-9 text-slate-400">%</span>
              </div>
  
              <div data-aos="fade-up" >
                <label class="block text-sm text-slate-600 mb-1">Loan Term</label>
                <select
                  v-model="newLoan.term"
                  class="w-full px-4 py-2 border border-gray-200 rounded-lg focus:ring-2 focus:ring-sky-400 focus:border-transparent appearance-none bg-white"
                >
                  <option value="2">2 Years</option>
                  <option value="3">3 Years</option>
                  <option value="5">5 Years</option>
                </select>
              </div>
            </div>
          </div>
  
          <!-- Results Section -->
          <div data-aos="fade-up"  class="space-y-6">
            <h3 class="text-slate-800 text-xl font-semibold">
              3. Check the results
            </h3>
            
            <p class="text-slate-600">
              With an interest rate of {{ newLoan.rate }}% over {{ newLoan.term }} Years, 
              you will pay ${{ monthlyPayment }} per month and ${{ totalInterest }} in interest over
              the lifetime of your loan.
            </p>
  
            <!-- Savings Visualization -->
            <div class="space-y-8">
              <!-- Total Interest Savings -->
              <div class="flex items-center gap-8">
                <div data-aos="fade-up"  class="relative w-24 h-24">
                  <div class="w-full h-full rounded-full border-8 border-sky-100"></div>
                  <div class="absolute inset-0 flex items-center justify-center flex-col">
                    <span class="text-2xl font-bold text-sky-500">${{ interestSavings }}</span>
                    <span class="text-xs text-slate-500">Less in Interest</span>
                  </div>
                </div>
  
                <div data-aos="fade-up"  class="flex-1 space-y-4">
                  <div class="flex items-center justify-between">
                    <span class="text-slate-600">New Loan</span>
                    <span class="font-medium">${{ totalInterest }}</span>
                  </div>
                  <div class="w-full bg-gray-100 rounded-full h-2">
                    <div class="bg-slate-800 h-2 rounded-full" :style="`width: ${newLoanPercentage}%`"></div>
                  </div>
                  <div class="flex items-center justify-between">
                    <span class="text-slate-600">Current Loan</span>
                    <span class="font-medium">${{ currentTotalInterest }}</span>
                  </div>
                  <div class="w-full bg-gray-100 rounded-full h-2">
                    <div class="bg-sky-400 h-2 rounded-full" :style="`width: ${currentLoanPercentage}%`"></div>
                  </div>
                </div>
              </div>
  
              <!-- Monthly Payment Savings -->
              <div class="flex items-center gap-8">
                <div class="relative w-24 h-24">
                  <div class="w-full h-full rounded-full border-8 border-sky-100"></div>
                  <div class="absolute inset-0 flex items-center justify-center flex-col">
                    <span class="text-2xl font-bold text-sky-500">${{ monthlySavings }}</span>
                    <span class="text-xs text-slate-500">Less per month</span>
                  </div>
                </div>
  
                <div class="flex-1 space-y-4">
                  <div class="flex items-center justify-between">
                    <span class="text-slate-600">New Payment</span>
                    <span class="font-medium">${{ monthlyPayment }}</span>
                  </div>
                  <div class="w-full bg-gray-100 rounded-full h-2">
                    <div class="bg-slate-800 h-2 rounded-full" :style="`width: ${newMonthlyPercentage}%`"></div>
                  </div>
                  <div class="flex items-center justify-between">
                    <span class="text-slate-600">Current Payment</span>
                    <span class="font-medium">${{ currentMonthlyPayment }}</span>
                  </div>
                  <div class="w-full bg-gray-100 rounded-full h-2">
                    <div class="bg-sky-400 h-2 rounded-full" :style="`width: ${currentMonthlyPercentage}%`"></div>
                  </div>
                </div>
              </div>
            </div>
  
            <button class="w-full bg-slate-800 text-white py-4 rounded-xl hover:bg-slate-700 transition-colors">
              Check Rates
            </button>
  
            <p class="text-sm text-slate-500 text-center">
              Checking rate won't affect your credit score. Calculator results are for illustrative purposes only.
            </p>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, computed } from 'vue'
  
  const currentLoan = ref({
    amount: 1000,
    rate: 10.00,
    term: 2
  })
  
  const newLoan = ref({
    rate: 2.00,
    term: 3
  })
  
  // Computed values for loan calculations
  const monthlyPayment = computed(() => {
    // Implement actual loan calculation here
    return '29'
  })
  
  const currentMonthlyPayment = computed(() => {
    // Implement actual loan calculation here
    return '46'
  })
  
  const totalInterest = computed(() => {
    // Implement actual loan calculation here
    return '31'
  })
  
  const currentTotalInterest = computed(() => {
    // Implement actual loan calculation here
    return '108'
  })
  
  const interestSavings = computed(() => {
    return Number(currentTotalInterest.value) - Number(totalInterest.value)
  })
  
  const monthlySavings = computed(() => {
    return Number(currentMonthlyPayment.value) - Number(monthlyPayment.value)
  })
  
  // Computed values for progress bars
  const newLoanPercentage = computed(() => {
    return (Number(totalInterest.value) / Number(currentTotalInterest.value)) * 100
  })
  
  const currentLoanPercentage = computed(() => 100)
  
  const newMonthlyPercentage = computed(() => {
    return (Number(monthlyPayment.value) / Number(currentMonthlyPayment.value)) * 100
  })
  
  const currentMonthlyPercentage = computed(() => 100)
  </script>
  
  <style scoped>
  select {
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' fill='none' viewBox='0 0 24 24' stroke='%236B7280'%3E%3Cpath stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M19 9l-7 7-7-7'%3E%3C/path%3E%3C/svg%3E");
    background-position: right 0.5rem center;
    background-repeat: no-repeat;
    background-size: 1.5em 1.5em;
  }
  </style>