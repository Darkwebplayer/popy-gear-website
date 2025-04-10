<script setup lang="ts">
import { onMounted } from 'vue';
import anime from 'animejs';

onMounted(() => {
  anime({
    targets: '.testimonial-card',
    translateY: [60, 0],
    opacity: [0, 1],
    delay: anime.stagger(200),
    duration: 1000,
    easing: 'easeOutQuad'
  });
});
</script>

<template>
  <section id="testimonials" class="w-full py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold text-gray-900 mb-4">What Our Clients Say</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Trusted by industry leaders worldwide
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="testimonial-card bg-white p-8 rounded-xl shadow-lg">
          <div class="mb-6">
            <svg class="h-8 w-8 text-blue-600" fill="currentColor" viewBox="0 0 24 24">
              <path d="M4.583 17.321C3.553 16.227 3 15 3 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179zm10 0C13.553 16.227 13 15 13 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179z"/>
            </svg>
          </div>
          <p class="text-gray-600 mb-6">
            WunderworkGmbH's custom elliptical gears solved a critical design challenge in our new racing bike drivetrain. Their engineering expertise and attention to detail are unmatched.
          </p>
          <div>
            <p class="font-semibold text-gray-900">Johan Berger</p>
            <p class="text-gray-600">Head of R&D, VeloTech Cycles</p>
          </div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-xl shadow-lg">
          <div class="mb-6">
            <svg class="h-8 w-8 text-blue-600" fill="currentColor" viewBox="0 0 24 24">
              <path d="M4.583 17.321C3.553 16.227 3 15 3 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179zm10 0C13.553 16.227 13 15 13 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179z"/>
            </svg>
          </div>
          <p class="text-gray-600 mb-6">
            The consistent quality and precision of WunderworkGmbH gears have allowed us to improve our textile machinery performance significantly. Their customization options give us exactly what we need every time.
          </p>
          <div>
            <p class="font-semibold text-gray-900">Maria Schmidt</p>
            <p class="text-gray-600">Production Manager, TextileTech Industries</p>
          </div>
        </div>

        <div class="testimonial-card bg-white p-8 rounded-xl shadow-lg">
          <div class="mb-6">
            <svg class="h-8 w-8 text-blue-600" fill="currentColor" viewBox="0 0 24 24">
              <path d="M4.583 17.321C3.553 16.227 3 15 3 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179zm10 0C13.553 16.227 13 15 13 13.011c0-3.5 2.457-6.637 6.03-8.188l.893 1.378c-3.335 1.804-3.987 4.145-4.247 5.621.537-.278 1.24-.375 1.929-.311 1.804.167 3.226 1.648 3.226 3.489a3.5 3.5 0 01-3.5 3.5c-1.073 0-2.099-.49-2.748-1.179z"/>
            </svg>
          </div>
          <p class="text-gray-600 mb-6">
            When our aerospace application required a specialized motion profile that seemed impossible to achieve mechanically, WunderworkGmbH delivered a solution that exceeded our expectations.
          </p>
          <div>
            <p class="font-semibold text-gray-900">Dr. Thomas Wei</p>
            <p class="text-gray-600">Systems Engineer, AeroSystems International</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>