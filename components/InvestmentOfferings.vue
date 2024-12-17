<!-- components/InvestmentOfferings.vue -->
<template>
    <section class="max-w-6xl mx-auto px-4 py-16">
      <!-- Header -->
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 data-aos="fade-up" class="text-4xl font-bold text-gray-900 mb-4">Offerings open for investment</h2>
        <p data-aos="fade-up" class="text-gray-600">
          Explore pre-vetted investment opportunities available in a growing number of industry categories.
        </p>
      </div>
  
      <!-- Cards Grid -->
      <div data-aos="fade-up"  class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <InvestmentCard 
          v-for="project in projects" 
          :key="project.id" 
          :project="project"
        />
      </div>
  
      <!-- View All Button -->
      <div data-aos="fade-up"  class="text-center mt-12">
        <button class="border-2 border-pink-400 text-pink-400 px-8 py-3 uppercase hover:bg-pink-50 transition-colors">
          View all projects
        </button>
      </div>
    </section>
  </template>
  
  <script setup lang="ts">
  import investment from '@/assets/img/investment.png'
    import investment1 from '@/assets/img/invest1.png'
      import investment2 from '@/assets/img/invest2.png'
        import investment3 from '@/assets/img/invest3.png'
          import investment4 from '@/assets/img/invest4.png'
  interface Project {
    id: number;
    title: string;
    location: string;
    description: string;
    image: string;
    tags: string[];
    raised: number;
    goal: number;
    securityType: string;
    investmentMultiple: string;
    maturity: string;
    minInvestment: number;
  }
  
  const projects = ref<Project[]>([
    {
  id: 1,
  title: 'Maximum Yield Note',
  location: 'Grow your portfolio with compound interests!',
  description: 'The Maximum Yield Note offers you an opportunity to invest a lump sum amount and grow it over a period, earning good returns through compound interests in the process. It typically provides a significantly higher rate of return compared to the average yield of similar low-risk instruments in the fixed-income market.',
  image: investment, // Ensure `investment` is correctly linked to your image file or asset
  tags: ['COMPOUND INTEREST', 'FIXED-INCOME'], // Updated to 2 tags
  raised: 574920,
  goal: 1000000,
  securityType: 'Revenue Sharing Note',
  investmentMultiple: '1.4x',
  maturity: '48 Months', // Corresponds to "A minimum tenor of 2 years"
  minInvestment: 1000000, // Minimum investment specified as ₦1 million
  features: {
    interestRate: 'Up to 26%',
    returnCapitalisation: 'Capitalised monthly',
    payoutOptions: ['Monthly', 'Quarterly', 'Bi-Annually'],
    earlyLiquidationPenalty: 'Forfeiture of entire accrued interest'
  },
  investorProfile: 'Any investor who wants to see their investment portfolio grow over time, earning good returns in the process.'
},

    // {
    //   id: 1,
    //   title: 'Maximum Yield Note',
    //   location: 'Grow your portfolio with compound interests!',
    //   description: 'A recognized leader in language immersion & early education, opening second school.',
    //   image: investment,
    //   tags: ['HOUSE', 'FAMILY BUSINESS'],
    //   raised: 574920,
    //   goal: 1000000,
    //   securityType: 'Revenue Sharing Note',
    //   investmentMultiple: '1.4x',
    //   maturity: '48 Months',
    //   minInvestment: 100
    // },
    {
      id: 1,
      title: 'Oxalis',
      location: 'Brooklyn, NY',
      description: 'A recognized leader in language immersion & early education, opening second school.',
      image: investment1,
      tags: ['HOUSE', 'FAMILY BUSINESS'],
      raised: 574920,
      goal: 1000000,
      securityType: 'Revenue Sharing Note',
      investmentMultiple: '1.4x',
      maturity: '48 Months',
      minInvestment: 100
    },
    {
      id: 1,
      title: 'Oxalis',
      location: 'Brooklyn, NY',
      description: 'A recognized leader in language immersion & early education, opening second school.',
      image: investment2,
      tags: ['HOUSE', 'FAMILY BUSINESS'],
      raised: 574920,
      goal: 1000000,
      securityType: 'Revenue Sharing Note',
      investmentMultiple: '1.4x',
      maturity: '48 Months',
      minInvestment: 100
    },
    {
      id: 1,
      title: 'Oxalis',
      location: 'Brooklyn, NY',
      description: 'A recognized leader in language immersion & early education, opening second school.',
      image: investment3,
      tags: ['HOUSE', 'FAMILY BUSINESS'],
      raised: 574920,
      goal: 1000000,
      securityType: 'Revenue Sharing Note',
      investmentMultiple: '1.4x',
      maturity: '48 Months',
      minInvestment: 100
    },
    {
      id: 1,
      title: 'Oxalis',
      location: 'Brooklyn, NY',
      description: 'A recognized leader in language immersion & early education, opening second school.',
      image: investment4,
      tags: ['HOUSE', 'FAMILY BUSINESS'],
      raised: 574920,
      goal: 1000000,
      securityType: 'Revenue Sharing Note',
      investmentMultiple: '1.4x',
      maturity: '48 Months',
      minInvestment: 100
    },
    {
      id: 1,
      title: 'Oxalis',
      location: 'Brooklyn, NY',
      description: 'A recognized leader in language immersion & early education, opening second school.',
      image: investment3,
      tags: ['HOUSE', 'FAMILY BUSINESS'],
      raised: 574920,
      goal: 1000000,
      securityType: 'Revenue Sharing Note',
      investmentMultiple: '1.4x',
      maturity: '48 Months',
      minInvestment: 100
    },
  ]);
  </script>