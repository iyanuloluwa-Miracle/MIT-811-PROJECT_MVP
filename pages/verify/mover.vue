<template>
  <div class="min-h-screen flex flex-col items-center justify-center bg-gradient-to-br from-slate-50 to-slate-100 p-8">
    <div class="bg-white rounded-2xl shadow-xl border border-slate-200 p-8 w-full max-w-md">
      <h2 class="text-2xl font-bold text-slate-800 mb-4 text-center">Mover Verification</h2>
      <p class="mb-4 text-slate-600 text-center">Submit your documents to get verified as a trusted mover on the platform.</p>
      <form class="space-y-4">
        <div>
          <label class="block mb-1 font-semibold text-slate-700">Full Name</label>
          <input type="text" class="w-full border border-slate-200 rounded px-3 py-2" placeholder="Enter your full name" />
        </div>
        <div>
          <label class="block mb-1 font-semibold text-slate-700">Matric/ID Number</label>
          <input type="text" class="w-full border border-slate-200 rounded px-3 py-2" placeholder="Enter your matric or ID number" />
        </div>
        <div>
          <label class="block mb-1 font-semibold text-slate-700">Upload ID Document</label>
          <input type="file" class="w-full border border-slate-200 rounded px-3 py-2" />
        </div>
        <div>
          <label class="block mb-1 font-semibold text-slate-700">Upload Proof of Residence</label>
          <input type="file" class="w-full border border-slate-200 rounded px-3 py-2" />
        </div>
        <button type="button" class="w-full bg-gradient-to-r from-slate-600 to-slate-400 hover:from-slate-700 hover:to-slate-500 text-white py-2 rounded-lg font-bold shadow-lg transition-all duration-200">Submit for Verification</button>
      </form>
    </div>
  </div>
</template>
