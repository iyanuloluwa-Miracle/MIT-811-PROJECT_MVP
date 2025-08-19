<template>
  <nav class="bg-white/90 shadow-sm mb-8 border-b border-slate-100 sticky top-0 z-50 backdrop-blur">
    <div class="max-w-6xl mx-auto px-4 py-2 flex justify-between items-center">
      <NuxtLink to="/" class="flex items-center gap-2 font-extrabold text-xl md:text-2xl text-slate-800 tracking-tight">
        <img src="/favicon.ico" alt="Logo" class="w-6 h-6 md:w-8 md:h-8 rounded-full border border-slate-200 shadow-sm" />
        <span class="hidden sm:inline">Peer Housing</span>
        <span class="sm:hidden">Peer</span>
      </NuxtLink>
      
      <!-- Mobile menu button -->
      <button @click="toggleMenu" class="md:hidden p-2 rounded-md text-slate-700 hover:bg-slate-100">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
        </svg>
      </button>

      <!-- Desktop menu -->
      <div class="hidden md:flex gap-2 md:gap-4 items-center bg-slate-50 px-3 py-1 rounded-full border border-slate-200 shadow-sm">
        <NuxtLink to="/listings" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Search</NuxtLink>
        <NuxtLink to="/listings/create" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Create Listing</NuxtLink>
        <NuxtLink to="/auth/signin" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Sign In</NuxtLink>
        <NuxtLink to="/auth/signup" class="px-3 py-1 rounded-full text-white font-semibold bg-slate-700 hover:bg-slate-800 transition">Sign Up</NuxtLink>
      </div>
    </div>

    <!-- Mobile menu -->
    <div v-show="showMenu" class="md:hidden bg-white border-t border-slate-100 px-4 py-4 space-y-2">
      <NuxtLink to="/listings" class="block px-3 py-2 rounded-md text-slate-700 font-medium hover:bg-slate-100 transition" @click="closeMenu">Search</NuxtLink>
      <NuxtLink to="/listings/create" class="block px-3 py-2 rounded-md text-slate-700 font-medium hover:bg-slate-100 transition" @click="closeMenu">Create Listing</NuxtLink>
      <NuxtLink to="/auth/signin" class="block px-3 py-2 rounded-md text-slate-700 font-medium hover:bg-slate-100 transition" @click="closeMenu">Sign In</NuxtLink>
      <NuxtLink to="/auth/signup" class="block px-3 py-2 rounded-md text-white font-semibold bg-slate-700 hover:bg-slate-800 transition text-center" @click="closeMenu">Sign Up</NuxtLink>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const showMenu = ref(false)

const toggleMenu = () => {
  showMenu.value = !showMenu.value
}

const closeMenu = () => {
  showMenu.value = false
}
</script>
