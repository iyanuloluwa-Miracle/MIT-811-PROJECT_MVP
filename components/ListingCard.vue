<template>
  <div class="bg-white rounded-2xl shadow-xl border border-blue-100 p-6 flex flex-col group hover:shadow-2xl transition-all duration-200">
    <!-- Dummy Listing Image -->
    <img
      :src="imageSrc"
      alt="Listing image"
      class="w-full h-40 object-cover rounded-xl mb-4 border border-slate-100"
    />
    <div class="flex items-center gap-3 mb-2">
      <div class="bg-blue-100 text-blue-700 rounded-full p-2">
        <slot name="icon" />
      </div>
      <h3 class="text-xl font-bold text-blue-800">{{ title }}</h3>
      <span class="inline-block bg-green-100 text-green-700 text-xs px-2 py-1 rounded-full font-semibold ml-2">Verified</span>
    </div>
    <p class="mb-2 text-gray-700">{{ description }}</p>
    <div class="flex flex-wrap gap-2 mb-2 text-sm">
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ location }}</span>
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ type }}</span>
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">${{ price }}/mo</span>
    </div>
    <!-- Dummy review/rating section -->
    <div class="mb-2">
      <div class="flex items-center gap-1 mb-1">
        <span class="text-yellow-400">★</span><span class="text-yellow-400">★</span><span class="text-yellow-400">★</span><span class="text-yellow-400">★</span><span class="text-gray-300">★</span>
        <span class="text-xs text-gray-500 ml-2">4.0 (2 reviews)</span>
      </div>
      <div class="text-xs text-gray-600 italic mb-1">"Great place, very responsive mover!"</div>
      <div class="text-xs text-gray-600 italic mb-1">"Clean and quiet, would rent again."</div>
      <button class="text-blue-600 text-xs underline mt-1">Leave a review</button>
    </div>
    <NuxtLink :to="contactLink" class="mt-2 text-blue-600 font-semibold hover:underline self-start">Contact Mover</NuxtLink>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{ title: string, description: string, location: string, type: string, price: number, contactLink: string }>()

// Dummy images for each type
const typeImages: Record<string, string> = {
  Apartment: 'https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80',
  House: 'https://images.unsplash.com/photo-1568605114967-8130f3a36994?auto=format&fit=crop&w=400&q=80',
  Room: 'https://images.unsplash.com/photo-1512918728675-ed5a9ecdebfd?auto=format&fit=crop&w=400&q=80',
  Default: 'https://images.unsplash.com/photo-1460518451285-97b6aa326961?auto=format&fit=crop&w=400&q=80',
}
const imageSrc = typeImages[props.type] || typeImages.Default
</script>
