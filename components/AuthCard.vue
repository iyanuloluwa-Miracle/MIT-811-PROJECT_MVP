<template>
  <div class="w-full max-w-sm p-8 bg-white rounded-2xl shadow-2xl border border-blue-100">
    <div class="flex flex-col items-center mb-6">
      <div class="bg-blue-100 text-blue-700 rounded-full p-3 mb-2">
        <slot name="icon" />
      </div>
      <h2 class="text-2xl font-extrabold text-blue-800">{{ title }}</h2>
    </div>
    <form class="space-y-5">
      <slot />
    </form>
    <p class="mt-6 text-center text-sm">
      <slot name="footer" />
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{ title: string }>()
</script>
