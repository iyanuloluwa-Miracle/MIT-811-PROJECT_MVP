<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100 py-10">
    <div class="w-full max-w-md p-8 bg-white rounded-2xl shadow-2xl border border-blue-100 mb-8">
      <div class="flex items-center gap-4 mb-4">
        <div class="bg-blue-100 text-blue-700 rounded-full p-4">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-10 w-10' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M5.121 17.804A13.937 13.937 0 0112 15c2.485 0 4.797.755 6.879 2.047M15 10a3 3 0 11-6 0 3 3 0 016 0z' /></svg>
        </div>
        <div>
          <h2 class="text-2xl font-bold text-blue-800">Jane Doe</h2>
          <span class="inline-block bg-green-100 text-green-700 text-xs px-2 py-1 rounded-full font-semibold mt-1">Verified Mover</span>
        </div>
      </div>
      <div class="mb-2 text-gray-700"><span class="font-semibold">Email:</span> jane.doe@email.com</div>
      <div class="mb-2 text-gray-700"><span class="font-semibold">Role:</span> Mover</div>
      <div class="mb-2 text-gray-700"><span class="font-semibold">Bio:</span> Friendly and responsive mover, loves helping people find great homes.</div>
    </div>
    <div class="w-full max-w-2xl">
      <h3 class="text-xl font-bold text-blue-800 mb-4">My Listings</h3>
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <ListingCard
          v-for="listing in myListings"
          :key="listing.id"
          :title="listing.title"
          :description="listing.description"
          :location="listing.location"
          :type="listing.type"
          :price="listing.price"
          :contactLink="'/contact'"
        >
          <template #icon>
            <svg v-if="listing.type === 'Apartment'" xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M3 10h1v10h16V10h1M4 10V4a1 1 0 011-1h2a1 1 0 011 1v6m8 0V4a1 1 0 011-1h2a1 1 0 011 1v6' /></svg>
            <svg v-else-if="listing.type === 'House'" xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M3 12l2-2m0 0l7-7 7 7m-9 2v6m4-6v6m5 6H5a2 2 0 01-2-2V10a2 2 0 012-2h14a2 2 0 012 2v10a2 2 0 01-2 2z' /></svg>
            <svg v-else xmlns='http://www.w3.org/2000/svg' class='h-6 w-6' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M8 10h.01M12 10h.01M16 10h.01M9 16h6m2 4H7a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v12a2 2 0 01-2 2z' /></svg>
          </template>
        </ListingCard>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import ListingCard from '~/components/ListingCard.vue'
const myListings = [
  {
    id: 1,
    title: 'Sunny Apartment in City Center',
    description: 'Spacious 2-bedroom apartment with lots of sunlight and close to amenities.',
    location: 'Downtown',
    price: '1.2M',
    type: 'Apartment',
  },
  {
    id: 2,
    title: 'Cozy Room in Shared House',
    description: 'Affordable room in a friendly shared house.',
    location: 'Suburb',
    price: '1.8M',
    type: 'Room',
  },
]
</script>
