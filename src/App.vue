<script setup lang="ts">
import NavBar from './components/NavBar.vue';
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProductsSection from './components/ProductsSection.vue';
import CustomizationSection from './components/CustomizationSection.vue';
import TestimonialsSection from './components/TestimonialsSection.vue';
import ContactSection from './components/ContactSection.vue';
import Footer from './components/Footer.vue';
</script>

<template>
  <NavBar />
  <main class="w-full">
    <HeroSection />
    <AboutSection />
    <ProductsSection />
    <CustomizationSection />
    <TestimonialsSection />
    <ContactSection />
  </main>
  <Footer />
</template>

<style>
@tailwind base;
@tailwind components;
@tailwind utilities;

html {
  scroll-behavior: smooth;
}

body {
  @apply bg-white text-gray-900 w-full min-h-screen m-0 p-0;
}

#app {
  @apply w-full min-h-screen;
}
</style>