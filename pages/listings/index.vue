<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 to-blue-100 p-8">
    <div class="max-w-5xl mx-auto">
      <h2 class="text-3xl font-extrabold text-blue-800 mb-8 text-center drop-shadow">Find a Home</h2>
      <div class="mb-8 flex flex-col md:flex-row gap-4 justify-center items-center bg-white rounded-xl shadow-lg p-6 border border-blue-100">
        <input type="text" placeholder="Location" class="border border-blue-200 rounded px-4 py-2 focus:ring-2 focus:ring-blue-200 w-full md:w-56" v-model="search.location" />
        <select v-model="search.type" class="border border-blue-200 rounded px-4 py-2 focus:ring-2 focus:ring-blue-200 w-full md:w-40">
          <option value="">All Types</option>
          <option value="Apartment">Apartment</option>
          <option value="House">House</option>
          <option value="Room">Room</option>
        </select>
        <button class="bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white px-6 py-2 rounded-lg font-bold shadow transition-all duration-200 w-full md:w-auto" @click="applyFilter">Search</button>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div v-for="listing in filteredListings" :key="listing.id" class="bg-white rounded-2xl shadow-xl border border-blue-100 p-6 flex flex-col group hover:shadow-2xl transition-all duration-200">
          <!-- Dummy Listing Image -->
          <img
            :src="getImageSrc(listing.type)"
            alt="Listing image"
            class="w-full h-40 object-cover rounded-xl mb-4 border border-slate-100"
          />
          <div class="flex items-center gap-3 mb-2">
            <div class="bg-blue-100 text-blue-700 rounded-full p-2">
              <svg v-if="listing.type === 'Apartment'" xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M3 10h1v10h16V10h1M4 10V4a1 1 0 011-1h2a1 1 0 011 1v6m8 0V4a1 1 0 011-1h2a1 1 0 011 1v6' /></svg>
              <svg v-else-if="listing.type === 'House'" xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M3 12l2-2m0 0l7-7 7 7m-9 2v6m4-6v6m5 6H5a2 2 0 01-2-2V10a2 2 0 012-2h14a2 2 0 012 2v10a2 2 0 01-2 2z' /></svg>
              <svg v-else xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M8 10h.01M12 10h.01M16 10h.01M9 16h6m2 4H7a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v12a2 2 0 01-2 2z' /></svg>
            </div>
            <h3 class="text-xl font-bold text-blue-800">{{ listing.title }}</h3>
          </div>
          <p class="mb-2 text-gray-700">{{ listing.description }}</p>
          <div class="flex flex-wrap gap-2 mb-2 text-sm">
            <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ listing.location }}</span>
            <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">{{ listing.type }}</span>
            <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded">${{ listing.price }}/mo</span>
          </div>
          <NuxtLink :to="'/contact'" class="mt-2 text-blue-600 font-semibold hover:underline self-start">Contact Landlord</NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
// Dummy images for each type
function getImageSrc(type: string) {
  const typeImages: Record<string, string> = {
    Apartment: 'https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80',
    House: 'https://images.unsplash.com/photo-1568605114967-8130f3a36994?auto=format&fit=crop&w=400&q=80',
    Room: 'https://images.unsplash.com/photo-1512918728675-ed5a9ecdebfd?auto=format&fit=crop&w=400&q=80',
    Default: 'https://images.unsplash.com/photo-1460518451285-97b6aa326961?auto=format&fit=crop&w=400&q=80',
  }
  return typeImages[type] || typeImages.Default
}
import { ref, computed } from 'vue'
const listings = ref([
  {
    id: 1,
    title: 'Sunny Apartment in City Center',
    description: 'Spacious 2-bedroom apartment with lots of sunlight and close to amenities.',
    location: 'Downtown',
    price: 1200,
    type: 'Apartment',
  },
  {
    id: 2,
    title: 'Cozy Room in Shared House',
    description: 'Affordable room in a friendly shared house.',
    location: 'Suburb',
    price: 500,
    type: 'Room',
  },
  {
    id: 3,
    title: 'Family House with Garden',
    description: '3-bedroom house with a large garden, perfect for families.',
    location: 'Uptown',
    price: 1800,
    type: 'House',
  },
])
const search = ref({ location: '', type: '' })
const filteredListings = computed(() => {
  return listings.value.filter(l => {
    const matchesLocation = !search.value.location || l.location.toLowerCase().includes(search.value.location.toLowerCase())
    const matchesType = !search.value.type || l.type === search.value.type
    return matchesLocation && matchesType
  })
})
function applyFilter() {}
</script>
