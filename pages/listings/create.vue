<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100">
    <AuthCard title="Create Listing">
      <template #icon>
        <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M9 17v-6a2 2 0 012-2h2a2 2 0 012 2v6m-6 0h6' /></svg>
      </template>
      <div class="flex items-center gap-2 mb-2">
        <span class="inline-block bg-green-100 text-green-700 text-xs px-2 py-1 rounded-full font-semibold">Verified</span>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Title</label>
        <input type="text" class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" value="Sunny Apartment in City Center" disabled />
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Description</label>
        <textarea class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" rows="3" disabled>Spacious 2-bedroom apartment with lots of sunlight and close to amenities.</textarea>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Location</label>
          <input type="text" class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" value="Downtown" disabled />
        </div>
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Price (per month)</label>
          <input type="number" class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" value="1200" disabled />
        </div>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Type</label>
        <select class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" disabled>
          <option selected>Apartment</option>
          <option>House</option>
          <option>Room</option>
        </select>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Utilities Included</label>
        <div class="flex gap-2 flex-wrap">
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">Water</span>
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">Electricity</span>
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">WiFi</span>
        </div>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Facilities</label>
        <div class="flex gap-2 flex-wrap">
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">Parking</span>
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">Laundry</span>
          <span class="bg-blue-50 text-blue-700 px-2 py-1 rounded text-xs">Gym</span>
        </div>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Mover Notes</label>
        <textarea class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" rows="2" disabled>Friendly and responsive mover, quick to resolve issues.</textarea>
      </div>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Experience/Narrative</label>
        <textarea class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" rows="2" disabled>Had a great experience living here, quiet neighborhood and close to public transport.</textarea>
      </div>
      <button type="button" class="w-full bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200" disabled>Create Listing</button>
    </AuthCard>
  </div>
</template>

<script setup lang="ts">
import AuthCard from '~/components/AuthCard.vue'
</script>
