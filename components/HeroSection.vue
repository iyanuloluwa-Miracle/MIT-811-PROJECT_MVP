<template>
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
</template>
