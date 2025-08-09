<template>
  <div class="w-full max-w-sm p-8 bg-white rounded-2xl shadow-2xl border border-slate-200">
    <div class="flex flex-col items-center mb-6">
      <div class="bg-slate-100 text-slate-600 rounded-full p-3 mb-2">
        <slot name="icon" />
      </div>
      <h2 class="text-2xl font-extrabold text-slate-800">{{ title }}</h2>
    </div>
    <form class="space-y-5">
      <slot />
    </form>
    <p class="mt-6 text-center text-sm text-slate-500">
      <slot name="footer" />
    </p>
  </div>
</template>

<script setup lang="ts">
defineProps<{ title: string }>()
</script>
