<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100">
    <div class="w-full max-w-lg p-10 bg-white rounded-2xl shadow-2xl border border-blue-100">
      <div class="flex flex-col items-center mb-6">
        <div class="bg-blue-100 text-blue-700 rounded-full p-3 mb-2">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M9 17v-6a2 2 0 012-2h2a2 2 0 012 2v6m-6 0h6' /></svg>
        </div>
        <h2 class="text-2xl font-extrabold text-blue-800">Create Listing</h2>
      </div>
      <form class="space-y-6">
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
        <button type="button" class="w-full bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200" disabled>Create Listing</button>
      </form>
    </div>
  </div>
</template>
