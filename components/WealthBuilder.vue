<script setup lang="ts">
interface StepItem {
  number: string;
  title: string;
  description: string;
}

const steps: StepItem[] = [
  {
    number: "1",
    title: "Build your savings",
    description: "Consistently automate your savings while setting realistic goals."
  },
  {
    number: "2",
    title: "Invest deliberately",
    description: "Invest in our diverse range of assets that grow in value over time."
  },
  {
    number: "3",
    title: "Stay rich",
    description: "Protect your wealth by managing risk, seeking advice and making smart financial decisions."
  }
];

// Compute margin class based on index
const getMarginClass = (index: number) => {
  switch(index) {
    case 1:
      return 'ml-8';
    case 2:
      return 'ml-16';
    default:
      return '';
  }
}
</script>

<template>
  <div class="bg-white">
    <div class="container mx-auto px-4 py-12 md:py-20">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <!-- Left Column -->
        <div class="space-y-6">
          <h1 class="text-4xl md:text-6xl font-bold text-navy-900 leading-tight">
            Get a <span class="italic">little</span> richer<br class="hidden md:block" /> each day
          </h1>
          <p class="text-xl md:text-2xl text-navy-900 opacity-90">
            One small step today, a giant leap for tomorrow.
          </p>
          <button class="bg-blue-600 text-white px-8 py-3 rounded-lg font-medium hover:bg-blue-700 transition-colors">
            Start Building Wealth
          </button>
        </div>

        <!-- Right Column - Steps Chart -->
        <div class="relative">
          <div class="relative z-10 space-y-4">
            <div v-for="(step, index) in steps" 
                 :key="index" 
                 class="relative flex items-start gap-4"
                 :class="[getMarginClass(index), {'mt-8': index > 0}]">
              <!-- Step Content -->
              <div class="bg-white rounded-lg p-6 shadow-lg flex-grow relative z-10">
                <div class="flex justify-between items-start">
                  <div>
                    <h3 class="font-bold text-navy-900 text-lg mb-2">{{ step.title }}</h3>
                    <p class="text-gray-600">{{ step.description }}</p>
                  </div>
                  <div class="bg-blue-600 text-white w-8 h-8 rounded-full flex items-center justify-center font-bold shrink-0">
                    {{ step.number }}
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Background Steps -->
          <div class="absolute bottom-0 right-0 w-3/4 h-full z-0">
            <div class="relative h-full">
              <!-- Step 1 Bar -->
              <div class="absolute bottom-0 right-0 w-1/3 h-1/3 bg-blue-600"></div>
              <!-- Step 2 Bar -->
              <div class="absolute bottom-0 right-[33%] w-1/3 h-2/3 bg-blue-600"></div>
              <!-- Step 3 Bar -->
              <div class="absolute bottom-0 right-[66%] w-1/3 h-full bg-blue-600"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.text-navy-900 {
  color: #1a2b6d;
}
</style>