<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-100 via-white to-blue-200 flex flex-col">
    <HeroSection />

    <!-- Featured Listings Section -->
    <section class="max-w-6xl mx-auto px-4 pb-10">
      <h2 class="text-2xl md:text-3xl font-bold text-blue-800 mb-6 mt-4">Featured Listings</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <ListingCard
          v-for="listing in featuredListings"
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
    </section>

    <!-- Problem Statement and Solution Section -->
    <section class="max-w-4xl mx-auto my-16 p-8 bg-white rounded-xl shadow-lg">
      <h2 class="text-3xl font-bold mb-4 text-center text-blue-700">Why We Built This Platform</h2>
      <p class="text-lg mb-6 text-gray-700 text-center">
        <span class="font-semibold">Problem Statement:</span> Finding safe, affordable, and trustworthy housing is a major challenge for students and young professionals. Traditional rental platforms often lack transparency, verified listings, and a sense of community, leading to scams, privacy concerns, and a stressful search experience.
      </p>
      <p class="text-lg text-gray-700 text-center">
        <span class="font-semibold">Our Solution:</span> We created this peer-to-peer housing platform to connect movers directly with verified landlords and tenants. Our platform emphasizes trust, transparency, and community, featuring verified profiles, honest reviews, privacy controls, and a seamless search and contact experience—all in a beautiful, easy-to-use interface.
      </p>
    </section>

    <!-- Footer -->
    <footer class="w-full py-6 bg-blue-50 mt-16 border-t border-blue-100">
      <div class="max-w-4xl mx-auto flex flex-col md:flex-row items-center justify-between px-4">
        <span class="text-gray-500 text-sm">&copy; 2025 Peer Housing Platform. All rights reserved.</span>
        <div class="flex space-x-4 mt-2 md:mt-0">
          <a href="#" class="text-blue-600 hover:underline text-sm">About</a>
          <a href="#" class="text-blue-600 hover:underline text-sm">Contact</a>
          <a href="#" class="text-blue-600 hover:underline text-sm">Privacy Policy</a>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import HeroSection from '~/components/HeroSection.vue'
import FeatureSection from '~/components/FeatureSection.vue'
import FeatureCard from '~/components/FeatureCard.vue'
import ListingCard from '~/components/ListingCard.vue'

const featuredListings = [
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
]
</script>
