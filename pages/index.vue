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
              Investment plans that work

            </h2>
            <h1 data-aos="fade-up"  class="text-slate-800 text-4xl md:text-6xl font-bold leading-tight">
              Choose an investment option,<br />
              Take control of your financial future.
            </h1>
          </div>

          <div class="space-y-4">
            <div data-aos="fade-up"  class="flex items-center space-x-2">
              <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Earn up to 27% per annum.
              </span>
            </div>
            <div data-aos="fade-up"  class="flex items-center space-x-2">
              <svg class="w-5 h-5 text-green-500" fill="currentColor" viewBox="0 0 20 20">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd" />
              </svg>
              <span class="text-gray-700">Tenor from 90 days to 365 days.</span>
            </div>
          </div>

          <div class="space-y-4">
            <div data-aos="fade-up"  class="relative">
              <input 
                type="text" 
                placeholder="Enter amount (₦100)" 
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
            <span class="text-gray-600">Over ₦1 billion in investments</span>
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
  <InvestmentCalculator />
  <WealthBuilder />
  <InvestmentOfferings />
  <!-- <Section1 />
  <Section2 />
  <Section3 /> -->
  <div class="overflow-hidden bg-white">
  <div class="relative mx-auto max-w-7xl px-6 py-16 lg:px-8">
    <div class="absolute bottom-0 left-3/4 top-0 hidden w-screen bg-gray-50 lg:block"></div>
    <div class="mx-auto max-w-prose text-base lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-8">
      <div>
        <!-- <h2 class="text-lg font-semibold text-indigo-600">Case Study</h2> -->
        <h3 class="mt-2 text-3xl/8 font-bold tracking-tight text-gray-900 sm:text-4xl">Grow your portfolio with compound interests!</h3>
      </div>
    </div>
    <div class="mt-8 lg:grid lg:grid-cols-2 lg:gap-8">
      <div class="relative lg:col-start-2 lg:row-start-1">
        <svg class="absolute right-0 top-0 -mr-20 -mt-20 hidden lg:block" width="404" height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
          <defs>
            <pattern id="de316486-4a29-4312-bdfc-fbce2132a2c1" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="384" fill="url(#de316486-4a29-4312-bdfc-fbce2132a2c1)" />
        </svg>
        <div class="relative mx-auto max-w-prose text-base lg:max-w-none">
          <figure>
            <img class="aspect-[12/7] w-full h-96 rounded-lg object-cover shadow-lg lg:aspect-auto" src="@/assets/img/test1.png" alt="Whitney leaning against a railing on a downtown street" width="1184" height="1376">
            <!-- <figcaption class="mt-3 flex text-sm text-gray-500">
              <svg class="size-5 flex-none text-gray-400" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                <path fill-rule="evenodd" d="M1 8a2 2 0 0 1 2-2h.93a2 2 0 0 0 1.664-.89l.812-1.22A2 2 0 0 1 8.07 3h3.86a2 2 0 0 1 1.664.89l.812 1.22A2 2 0 0 0 16.07 6H17a2 2 0 0 1 2 2v7a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8Zm13.5 3a4.5 4.5 0 1 1-9 0 4.5 4.5 0 0 1 9 0ZM10 14a3 3 0 1 0 0-6 3 3 0 0 0 0 6Z" clip-rule="evenodd" />
              </svg>
              <span class="ml-2">Photograph by Marcus O’Leary</span>
            </figcaption> -->
          </figure>
        </div>
      </div>
      <div class="mt-8 lg:mt-0">
        <div class="mx-auto text-base/7 text-gray-500">
          <p class="text-lg/7">The Maximum Yield Note offers you an opportunity to invest 
a lump sum amount and grow it over a period, earning 
good returns through compound interests in the process. 
It typically provides a significantly higher rate of return 
compared to the average yield of similar low-risk instruments 
in the fixed-income market.
</p>
          <!-- <p class="mt-5">Sollicitudin tristique eros erat odio sed vitae, consequat turpis elementum. Lorem nibh vel, eget pretium arcu vitae. Eros eu viverra donec ut volutpat donec laoreet quam urna.</p>
          <p class="mt-5">Bibendum eu nulla feugiat justo, elit adipiscing. Ut tristique sit nisi lorem pulvinar. Urna, laoreet fusce nibh leo. Dictum et et et sit. Faucibus sed non gravida lectus dignissim imperdiet a.</p>
          <p class="mt-5">Dictum magnis risus phasellus vitae quam morbi. Quis lorem lorem arcu, metus, egestas netus cursus. In.</p>
          <ul role="list" class="mt-5 list-disc space-y-2 pl-6 marker:text-gray-300">
            <li class="pl-2">Quis elit egestas venenatis mattis dignissim.</li>
            <li class="pl-2">Cras cras lobortis vitae vivamus ultricies facilisis tempus.</li>
            <li class="pl-2">Orci in sit morbi dignissim metus diam arcu pretium.</li>
          </ul>
          <p class="mt-5">Rhoncus nisl, libero egestas diam fermentum dui. At quis tincidunt vel ultricies. Vulputate aliquet velit faucibus semper. Pellentesque in venenatis vestibulum consectetur nibh id. In id ut tempus egestas. Enim sit aliquam nec, a. Morbi enim fermentum lacus in. Viverra.</p>
          <h3 class="mt-8 text-xl/8 font-semibold text-gray-900">How we helped</h3>
          <p class="mt-3">Tincidunt integer commodo, cursus etiam aliquam neque, et. Consectetur pretium in volutpat, diam. Montes, magna cursus nulla feugiat dignissim id lobortis amet. Laoreet sem est phasellus eu proin massa, lectus. Diam rutrum posuere donec ultricies non morbi. Mi a platea auctor mi.</p>
          <p class="mt-5">Sagittis scelerisque nulla cursus in enim consectetur quam. Dictum urna sed consectetur neque tristique pellentesque. Blandit amet, sed aenean erat arcu morbi.</p> -->
        </div>
      </div>
    </div>
  </div>
  </div>



  <div class="overflow-hidden bg-white">
  <div class="relative mx-auto max-w-7xl px-6 py-16 lg:px-8">
    <div class="absolute bottom-0 left-3/4 top-0 hidden w-screen bg-gray-50 lg:block"></div>
    <div class="mx-auto max-w-prose text-base lg:grid lg:max-w-none lg:grid-cols-2 lg:gap-8">
      <div>
        <!-- <h2 class="text-lg font-semibold text-indigo-600">Case Study</h2> -->
        <h3 class="mt-2 text-3xl/8 font-bold tracking-tight text-gray-900 sm:text-4xl">Get pwrsonalised financial solutions</h3>
      </div>
    </div>
    <div class="mt-8 lg:grid lg:grid-cols-2 lg:gap-8">
      <div class="relative lg:col-start-2 lg:row-start-1">
        <svg class="absolute right-0 top-0 -mr-20 -mt-20 hidden lg:block" width="404" height="384" fill="none" viewBox="0 0 404 384" aria-hidden="true">
          <defs>
            <pattern id="de316486-4a29-4312-bdfc-fbce2132a2c1" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect width="404" height="384" fill="url(#de316486-4a29-4312-bdfc-fbce2132a2c1)" />
        </svg>
        <div class="relative mx-auto max-w-prose text-base lg:max-w-none">
          <figure>
            <img class="aspect-[12/7] w-full h-96 rounded-lg object-cover shadow-lg lg:aspect-auto" src="@/assets/img/test2.png" alt="Whitney leaning against a railing on a downtown street" width="1184" height="1376">
            <!-- <figcaption class="mt-3 flex text-sm text-gray-500">
              <svg class="size-5 flex-none text-gray-400" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true" data-slot="icon">
                <path fill-rule="evenodd" d="M1 8a2 2 0 0 1 2-2h.93a2 2 0 0 0 1.664-.89l.812-1.22A2 2 0 0 1 8.07 3h3.86a2 2 0 0 1 1.664.89l.812 1.22A2 2 0 0 0 16.07 6H17a2 2 0 0 1 2 2v7a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2V8Zm13.5 3a4.5 4.5 0 1 1-9 0 4.5 4.5 0 0 1 9 0ZM10 14a3 3 0 1 0 0-6 3 3 0 0 0 0 6Z" clip-rule="evenodd" />
              </svg>
              <span class="ml-2">Photograph by Marcus O’Leary</span>
            </figcaption> -->
          </figure>
        </div>
      </div>
      <div class="mt-8 lg:mt-0">
        <div class="mx-auto text-base/7 text-gray-500">
          <p class="text-lg/7">Our commitment to personalized solutions, transaprent processes and unparralled customer support ensures your path to success is guided with expertise and trust
</p>
          <!-- <p class="mt-5">Sollicitudin tristique eros erat odio sed vitae, consequat turpis elementum. Lorem nibh vel, eget pretium arcu vitae. Eros eu viverra donec ut volutpat donec laoreet quam urna.</p>
          <p class="mt-5">Bibendum eu nulla feugiat justo, elit adipiscing. Ut tristique sit nisi lorem pulvinar. Urna, laoreet fusce nibh leo. Dictum et et et sit. Faucibus sed non gravida lectus dignissim imperdiet a.</p>
          <p class="mt-5">Dictum magnis risus phasellus vitae quam morbi. Quis lorem lorem arcu, metus, egestas netus cursus. In.</p>
          <ul role="list" class="mt-5 list-disc space-y-2 pl-6 marker:text-gray-300">
            <li class="pl-2">Quis elit egestas venenatis mattis dignissim.</li>
            <li class="pl-2">Cras cras lobortis vitae vivamus ultricies facilisis tempus.</li>
            <li class="pl-2">Orci in sit morbi dignissim metus diam arcu pretium.</li>
          </ul>
          <p class="mt-5">Rhoncus nisl, libero egestas diam fermentum dui. At quis tincidunt vel ultricies. Vulputate aliquet velit faucibus semper. Pellentesque in venenatis vestibulum consectetur nibh id. In id ut tempus egestas. Enim sit aliquam nec, a. Morbi enim fermentum lacus in. Viverra.</p>
          <h3 class="mt-8 text-xl/8 font-semibold text-gray-900">How we helped</h3>
          <p class="mt-3">Tincidunt integer commodo, cursus etiam aliquam neque, et. Consectetur pretium in volutpat, diam. Montes, magna cursus nulla feugiat dignissim id lobortis amet. Laoreet sem est phasellus eu proin massa, lectus. Diam rutrum posuere donec ultricies non morbi. Mi a platea auctor mi.</p>
          <p class="mt-5">Sagittis scelerisque nulla cursus in enim consectetur quam. Dictum urna sed consectetur neque tristique pellentesque. Blandit amet, sed aenean erat arcu morbi.</p> -->
        </div>
      </div>
    </div>
  </div>
  </div>

  <InvestmentStats />
  <SavingsCalculator />
  <CapitalRaisingSection />
  <FooterSection />
</main>
</template>

