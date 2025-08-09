<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100">
    <ContactCard>
      <template #icon>
        <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M21 15a2 2 0 01-2 2H5a2 2 0 01-2-2V7a2 2 0 012-2h14a2 2 0 012 2v8z' /></svg>
      </template>
      <template #listingInfo>
        <p class="font-semibold text-blue-700">Listing: <span class="text-gray-700">Sunny Apartment in City Center</span></p>
        <p class="font-semibold text-blue-700">Mover: <span class="text-gray-700">Jane Doe</span> <span class="inline-block bg-green-100 text-green-700 text-xs px-2 py-1 rounded-full font-semibold ml-1">Verified</span></p>
      </template>
      <div>
        <label class="block mb-1 font-semibold text-blue-700">Your Message</label>
        <textarea class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" rows="4" placeholder="Hi, I am interested in your listing. Is it still available?" disabled></textarea>
      </div>
      <div class="flex flex-col gap-2 my-3">
        <label class="inline-flex items-center text-sm text-blue-700">
          <input type="checkbox" class="form-checkbox mr-2" checked disabled /> Allow contact by email
        </label>
        <label class="inline-flex items-center text-sm text-blue-700">
          <input type="checkbox" class="form-checkbox mr-2" disabled /> Allow contact by phone
        </label>
        <label class="inline-flex items-center text-sm text-blue-700">
          <input type="checkbox" class="form-checkbox mr-2" checked disabled /> Hide my real name
        </label>
      </div>
      <button type="button" class="w-full bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200" disabled>Send Message</button>
    </ContactCard>
  </div>
</template>

<script setup lang="ts">
import ContactCard from '~/components/ContactCard.vue'
</script>
