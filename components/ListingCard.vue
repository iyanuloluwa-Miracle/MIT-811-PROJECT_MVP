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
      <span v-if="type === 'Agent'" class="bg-gradient-to-r from-purple-500 to-pink-500 text-white px-3 py-1 rounded-full text-xs font-bold flex items-center gap-1 shadow-md border-2 border-white animate-pulse">
        <svg xmlns='http://www.w3.org/2000/svg' class='h-4 w-4 inline' fill='currentColor' viewBox='0 0 20 20'><path d='M10 2a8 8 0 100 16 8 8 0 000-16zm3.93 6.36l-4.24 4.24a1 1 0 01-1.42 0l-2.12-2.12a1 1 0 111.42-1.42l1.41 1.41 3.53-3.53a1 1 0 111.42 1.42z'/></svg>
        Verified Agent
      </span>
      <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">₦{{ price }}/mo</span>
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

// Dummy images for each type (including Agent)
const typeImages: Record<string, string> = {
  Apartment: 'https://images.unsplash.com/photo-1598928636135-d146006ff4be?auto=format&fit=crop&w=400&q=80', // Modern African apartment (e.g., urban Nairobi or Lagos)
  House: 'https://images.unsplash.com/photo-1600585154340-be6161a56a0c?auto=format&fit=crop&w=400&q=80', // African house (e.g., traditional or modern suburban home)
  Room: 'https://images.unsplash.com/photo-1618221195710-dd2b64383520?auto=format&fit=crop&w=400&q=80', // African room (e.g., culturally decorated interior)
  Agent: 'https://images.unsplash.com/photo-1532094349884-543995b5f930?auto=format&fit=crop&w=400&q=80', // African professional (e.g., real estate agent in African context)
  Default: 'https://images.unsplash.com/photo-1598928636135-d146006ff4be?auto=format&fit=crop&w=400&q=80', // Fallback to modern African apartment
}
const imageSrc = typeImages[props.type] || typeImages.Default
</script>
