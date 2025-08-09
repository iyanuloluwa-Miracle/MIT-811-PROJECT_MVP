<template>
  <div class="bg-white rounded-2xl shadow-xl p-8 flex flex-col items-center group hover:shadow-2xl transition-all duration-200 border border-blue-100 hover:border-blue-300">
    <div class="bg-blue-100 text-blue-700 rounded-full p-4 mb-4 group-hover:bg-blue-600 group-hover:text-white transition-all duration-200">
      <slot name="icon" />
    </div>
    <h3 class="font-bold text-xl mb-2 text-blue-800">{{ title }}</h3>
    <p class="text-gray-600 text-base">{{ description }}</p>
    <NuxtLink :to="link" class="mt-4 text-blue-600 hover:underline text-base font-semibold">{{ linkText }}</NuxtLink>
  </div>
</template>

<script setup lang="ts">
defineProps<{ title: string, description: string, link: string, linkText: string }>()
</script>
