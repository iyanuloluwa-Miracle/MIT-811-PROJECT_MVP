<template>
  <div class="w-full max-w-md p-10 bg-white rounded-2xl shadow-2xl border border-blue-100">
    <div class="flex flex-col items-center mb-6">
      <div class="bg-blue-100 text-blue-700 rounded-full p-3 mb-2">
        <slot name="icon" />
      </div>
      <h2 class="text-2xl font-extrabold text-blue-800">Contact Landlord</h2>
    </div>
    <div class="mb-6">
      <slot name="listingInfo" />
    </div>
    <form class="space-y-5">
      <slot />
    </form>
    <p class="mt-6 text-center text-sm text-gray-500">(Static demo: messaging is not functional)</p>
  </div>
</template>
