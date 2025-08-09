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

    <FeatureSection>
      <FeatureCard
        title="Role-based Access"
        description="Sign up or sign in as a Tenant or Landlord for a tailored experience."
        link="/auth/signup"
        linkText="Get Started"
      >
        <template #icon>
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M5.121 17.804A13.937 13.937 0 0112 15c2.485 0 4.797.755 6.879 2.047M15 10a3 3 0 11-6 0 3 3 0 016 0z' /></svg>
        </template>
      </FeatureCard>
      <FeatureCard
        title="Create Listings"
        description="Landlords can easily create new housing listings with a simple form."
        link="/listings/create"
        linkText="Create Now"
      >
        <template #icon>
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M9 17v-6a2 2 0 012-2h2a2 2 0 012 2v6m-6 0h6' /></svg>
        </template>
      </FeatureCard>
      <FeatureCard
        title="Search & Filter"
        description="Find your perfect home with easy-to-use search and filter options."
        link="/listings"
        linkText="Browse"
      >
        <template #icon>
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M8 10h.01M12 10h.01M16 10h.01M9 16h6m2 4H7a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v12a2 2 0 01-2 2z' /></svg>
        </template>
      </FeatureCard>
      <FeatureCard
        title="Contact System"
        description="Message landlords or tenants directly from a listing page."
        link="/contact"
        linkText="See Demo"
      >
        <template #icon>
          <svg xmlns='http://www.w3.org/2000/svg' class='h-9 w-9' fill='none' viewBox='0 0 24 24' stroke='currentColor'><path stroke-linecap='round' stroke-linejoin='round' stroke-width='2' d='M21 15a2 2 0 01-2 2H5a2 2 0 01-2-2V7a2 2 0 012-2h14a2 2 0 012 2v8z' /></svg>
        </template>
      </FeatureCard>
    </FeatureSection>
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
