<template>
  <div class="bg-white rounded-2xl shadow-xl border border-blue-100 p-6 flex flex-col group hover:shadow-2xl transition-all duration-200">
    <div class="flex items-center gap-3 mb-2">
      <div class="bg-blue-100 text-blue-700 rounded-full p-2">
        <slot name="icon" />
      </div>
      <h3 class="text-xl font-bold text-blue-800">{{ title }}</h3>
    </div>
    <p class="mb-2 text-gray-700">{{ description }}</p>
    <div class="flex flex-wrap gap-2 mb-2 text-sm">
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ location }}</span>
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ type }}</span>
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">${{ price }}/mo</span>
    </div>
    <NuxtLink :to="contactLink" class="mt-2 text-blue-600 font-semibold hover:underline self-start">Contact Landlord</NuxtLink>
  </div>
</template>

<script setup lang="ts">
defineProps<{ title: string, description: string, location: string, type: string, price: number, contactLink: string }>()
</script>
