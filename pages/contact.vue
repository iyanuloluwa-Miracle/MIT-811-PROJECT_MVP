<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-blue-50 to-blue-100">
    <div class="w-full max-w-md p-10 bg-white rounded-2xl shadow-2xl border border-blue-100">
      <div class="flex flex-col items-center mb-6">
        <div class="bg-blue-100 text-blue-700 rounded-full p-3 mb-2">
          <svg xmlns='http://www.w3.org/2000/svg' class='h-8 w-8' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M21 15a2 2 0 01-2 2H5a2 2 0 01-2-2V7a2 2 0 012-2h14a2 2 0 012 2v8z' /></svg>
        </div>
        <h2 class="text-2xl font-extrabold text-blue-800">Contact Landlord</h2>
      </div>
      <div class="mb-6">
        <p class="font-semibold text-blue-700">Listing: <span class="text-gray-700">Sunny Apartment in City Center</span></p>
        <p class="font-semibold text-blue-700">Landlord: <span class="text-gray-700">Jane Doe</span></p>
      </div>
      <form class="space-y-5">
        <div>
          <label class="block mb-1 font-semibold text-blue-700">Your Message</label>
          <textarea class="w-full border border-blue-200 rounded px-3 py-2 bg-gray-50" rows="4" placeholder="Hi, I am interested in your listing. Is it still available?" disabled></textarea>
        </div>
        <button type="button" class="w-full bg-gradient-to-r from-blue-600 to-blue-400 hover:from-blue-700 hover:to-blue-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200" disabled>Send Message</button>
      </form>
      <p class="mt-6 text-center text-sm text-gray-500">(Static demo: messaging is not functional)</p>
    </div>
  </div>
</template>
