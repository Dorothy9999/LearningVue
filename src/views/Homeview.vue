<script setup>
import Hero from '@/components/Hero.vue';
import HomeCards from '@/components/HomeCards.vue';
import JobListings from '@/components/JobListings.vue';
</script>

<template>
    <Hero title="From mother title" />
    <HomeCards />
    <JobListings :limit="3" :show-button="true"></JobListings>
</template>