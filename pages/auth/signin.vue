<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100">
    <div class="w-full max-w-sm p-8 bg-white rounded-2xl shadow-2xl border border-blue-100">
      <div class="flex flex-col items-center mb-6">
        <div class="bg-blue-100 text-blue-700 rounded-full p-3 mb-2">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M5.121 17.804A13.937 13.937 0 0112 15c2.485 0 4.797.755 6.879 2.047M15 10a3 3 0 11-6 0 3 3 0 016 0z' /></svg>
        </div>
        <h2 class="text-2xl font-extrabold text-blue-800">Sign In</h2>
      </div>
      <form class="space-y-5">
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Role</label>
          <select v-model="role" class="w-full border border-blue-200 rounded px-3 py-2 focus:ring-2 focus:ring-blue-200">
            <option value="Tenant">Tenant</option>
            <option value="Landlord">Landlord</option>
          </select>
        </div>
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Email</label>
          <input type="email" class="w-full border border-blue-200 rounded px-3 py-2 focus:ring-2 focus:ring-blue-200" />
        </div>
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Password</label>
          <input type="password" class="w-full border border-blue-200 rounded px-3 py-2 focus:ring-2 focus:ring-blue-200" />
        </div>
        <button type="button" class="w-full bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200">Sign In</button>
      </form>
      <p class="mt-6 text-center text-sm">Don't have an account? <NuxtLink to="/auth/signup" class="text-blue-600 font-semibold hover:underline">Sign Up</NuxtLink></p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const role = ref('Tenant')
</script>
