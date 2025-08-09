<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-100 via-white to-blue-200 flex flex-col">
    <!-- Hero Section -->
    <section class="relative flex-1 flex flex-col items-center justify-center text-center py-20 px-4 overflow-hidden">
      <div class="absolute inset-0 pointer-events-none">
        <div class="absolute -top-32 -left-32 w-96 h-96 bg-blue-200 rounded-full opacity-30 blur-3xl animate-pulse"></div>
        <div class="absolute -bottom-32 -right-32 w-96 h-96 bg-blue-400 rounded-full opacity-20 blur-3xl animate-pulse"></div>
      </div>
      <h1 class="text-5xl md:text-6xl font-extrabold text-blue-900 mb-6 drop-shadow-lg tracking-tight">Find Your Next Home, Effortlessly</h1>
      <p class="text-xl md:text-2xl text-gray-700 mb-10 max-w-2xl mx-auto">Peer-to-peer housing made simple. Browse listings, connect with landlords or tenants, and manage your housing journey—all in one place.</p>
      <div class="flex flex-col md:flex-row gap-6 justify-center mb-14 z-10">
        <NuxtLink to="/listings" class="transition-all duration-200 bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white px-10 py-4 rounded-xl font-bold shadow-lg hover:scale-105 focus:outline-none focus:ring-4 focus:ring-blue-200">Browse Listings</NuxtLink>
        <NuxtLink to="/listings/create" class="transition-all duration-200 bg-white border-2 border-blue-600 text-blue-700 px-10 py-4 rounded-xl font-bold shadow-lg hover:bg-blue-50 hover:scale-105 focus:outline-none focus:ring-4 focus:ring-blue-200">Create Listing</NuxtLink>
      </div>
    </section>

    <!-- Features Section -->
    <section class="relative max-w-6xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8 px-4 pb-20 z-10">
      <div class="bg-white rounded-2xl shadow-xl p-8 flex flex-col items-center group hover:shadow-2xl transition-all duration-200 border border-blue-100 hover:border-blue-300">
        <div class="bg-blue-100 text-blue-700 rounded-full p-4 mb-4 group-hover:bg-blue-600 group-hover:text-white transition-all duration-200">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M5.121 17.804A13.937 13.937 0 0112 15c2.485 0 4.797.755 6.879 2.047M15 10a3 3 0 11-6 0 3 3 0 016 0z' /></svg>
        </div>
        <h3 class="font-bold text-xl mb-2 text-blue-800">Role-based Access</h3>
        <p class="text-gray-600 text-base">Sign up or sign in as a Tenant or Landlord for a tailored experience.</p>
        <NuxtLink to="/auth/signup" class="mt-4 text-blue-600 hover:underline text-base font-semibold">Get Started</NuxtLink>
      </div>
      <div class="bg-white rounded-2xl shadow-xl p-8 flex flex-col items-center group hover:shadow-2xl transition-all duration-200 border border-blue-100 hover:border-blue-300">
        <div class="bg-blue-100 text-blue-700 rounded-full p-4 mb-4 group-hover:bg-blue-600 group-hover:text-white transition-all duration-200">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M9 17v-6a2 2 0 012-2h2a2 2 0 012 2v6m-6 0h6' /></svg>
        </div>
        <h3 class="font-bold text-xl mb-2 text-blue-800">Create Listings</h3>
        <p class="text-gray-600 text-base">Landlords can easily create new housing listings with a simple form.</p>
        <NuxtLink to="/listings/create" class="mt-4 text-blue-600 hover:underline text-base font-semibold">Create Now</NuxtLink>
      </div>
      <div class="bg-white rounded-2xl shadow-xl p-8 flex flex-col items-center group hover:shadow-2xl transition-all duration-200 border border-blue-100 hover:border-blue-300">
        <div class="bg-blue-100 text-blue-700 rounded-full p-4 mb-4 group-hover:bg-blue-600 group-hover:text-white transition-all duration-200">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M8 10h.01M12 10h.01M16 10h.01M9 16h6m2 4H7a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v12a2 2 0 01-2 2z' /></svg>
        </div>
        <h3 class="font-bold text-xl mb-2 text-blue-800">Search & Filter</h3>
        <p class="text-gray-600 text-base">Find your perfect home with easy-to-use search and filter options.</p>
        <NuxtLink to="/listings" class="mt-4 text-blue-600 hover:underline text-base font-semibold">Browse</NuxtLink>
      </div>
      <div class="bg-white rounded-2xl shadow-xl p-8 flex flex-col items-center group hover:shadow-2xl transition-all duration-200 border border-blue-100 hover:border-blue-300">
        <div class="bg-blue-100 text-blue-700 rounded-full p-4 mb-4 group-hover:bg-blue-600 group-hover:text-white transition-all duration-200">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M21 15a2 2 0 01-2 2H5a2 2 0 01-2-2V7a2 2 0 012-2h14a2 2 0 012 2v8z' /></svg>
        </div>
        <h3 class="font-bold text-xl mb-2 text-blue-800">Contact System</h3>
        <p class="text-gray-600 text-base">Message landlords or tenants directly from a listing page.</p>
        <NuxtLink to="/contact" class="mt-4 text-blue-600 hover:underline text-base font-semibold">See Demo</NuxtLink>
      </div>
    </section>
  </div>
</template>
