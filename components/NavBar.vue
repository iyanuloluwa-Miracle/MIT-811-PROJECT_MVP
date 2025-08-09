<template>
  <nav class="bg-white/90 shadow-sm mb-8 border-b border-slate-100 sticky top-0 z-50 backdrop-blur">
    <div class="max-w-6xl mx-auto px-4 py-2 flex justify-between items-center">
      <NuxtLink to="/" class="flex items-center gap-2 font-extrabold text-2xl text-slate-800 tracking-tight">
        <img src="/favicon.ico" alt="Logo" class="w-8 h-8 rounded-full border border-slate-200 shadow-sm" />
        Peer Housing
      </NuxtLink>
      <div class="flex gap-2 md:gap-4 items-center bg-slate-50 px-3 py-1 rounded-full border border-slate-200 shadow-sm">
        <NuxtLink to="/listings" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Search</NuxtLink>
        <NuxtLink to="/listings/create" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Create Listing</NuxtLink>
        <NuxtLink to="/auth/signin" class="px-3 py-1 rounded-full text-slate-700 font-medium hover:bg-slate-100 transition">Sign In</NuxtLink>
        <NuxtLink to="/auth/signup" class="px-3 py-1 rounded-full text-white font-semibold bg-slate-700 hover:bg-slate-800 transition">Sign Up</NuxtLink>
      </div>
    </div>
  </nav>
</template>
