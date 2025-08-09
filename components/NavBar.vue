<template>
  <nav class="bg-white shadow mb-6">
    <div class="max-w-5xl mx-auto px-4 py-3 flex justify-between items-center">
      <NuxtLink to="/" class="font-bold text-xl text-blue-700">P2P Housing</NuxtLink>
      <div class="flex gap-4">
        <NuxtLink to="/listings" class="hover:underline">Search</NuxtLink>
        <NuxtLink to="/listings/create" class="hover:underline">Create Listing</NuxtLink>
        <NuxtLink to="/auth/signin" class="hover:underline">Sign In</NuxtLink>
        <NuxtLink to="/auth/signup" class="hover:underline">Sign Up</NuxtLink>
      </div>
    </div>
  </nav>
</template>
