
<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-slate-50 to-slate-100">
    <AuthCard title="Sign In">
      <template #icon>
        <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M5.121 17.804A13.937 13.937 0 0112 15c2.485 0 4.797.755 6.879 2.047M15 10a3 3 0 11-6 0 3 3 0 016 0z' /></svg>
      </template>
      <div>
  <label class="block mb-1 font-semibold text-slate-700">Role</label>
  <select v-model="role" class="w-full border border-slate-200 rounded px-3 py-2 focus:ring-2 focus:ring-slate-200">
    <option value="Tenant">Tenant</option>
    <option value="Landlord">Landlord</option>
    <option value="Agent">Agent</option>
  </select>
      </div>
      <div>
  <label class="block mb-1 font-semibold text-slate-700">Email</label>
  <input type="email" class="w-full border border-slate-200 rounded px-3 py-2 focus:ring-2 focus:ring-slate-200" />
      </div>
      <div>
  <label class="block mb-1 font-semibold text-slate-700">Password</label>
  <input type="password" class="w-full border border-slate-200 rounded px-3 py-2 focus:ring-2 focus:ring-slate-200" />
      </div>
  <button type="button" class="w-full bg-gradient-to-r from-slate-600 to-slate-400 hover:from-slate-700 hover:to-slate-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200">Sign In</button>
      <template #footer>
  Don't have an account? <NuxtLink to="/auth/signup" class="text-slate-600 font-semibold hover:underline">Sign Up</NuxtLink>
      </template>
    </AuthCard>
  </div>
</template>

<script setup lang="ts">
import AuthCard from '~/components/AuthCard.vue'
import { ref } from 'vue'
const role = ref('Tenant')
</script>
