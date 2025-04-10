<script setup lang="ts">
import { onMounted } from 'vue';
import anime from 'animejs';

onMounted(() => {
  anime({
    targets: '.feature-item',
    translateX: [-30, 0],
    opacity: [0, 1],
    delay: anime.stagger(100),
    duration: 800,
    easing: 'easeOutQuad'
  });
});
</script>

<template>
  <section id="customization" class="w-full py-24 bg-gradient-to-br from-blue-900 to-indigo-900 text-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold mb-4">Design Your Own Gears</h2>
        <p class="text-xl text-blue-200 max-w-3xl mx-auto">
          Your Vision, Our Precision
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <div class="space-y-6">
          <div class="feature-item bg-white/10 backdrop-blur-sm rounded-lg p-6">
            <h3 class="text-xl font-semibold mb-2">Custom Eccentricity</h3>
            <p class="text-blue-200">Define the exact motion profile you need</p>
          </div>
          
          <div class="feature-item bg-white/10 backdrop-blur-sm rounded-lg p-6">
            <h3 class="text-xl font-semibold mb-2">Material Selection</h3>
            <p class="text-blue-200">Choose from our extensive range of metals and advanced polymers</p>
          </div>
          
          <div class="feature-item bg-white/10 backdrop-blur-sm rounded-lg p-6">
            <h3 class="text-xl font-semibold mb-2">Surface Treatments</h3>
            <p class="text-blue-200">Select from various hardening and coating options</p>
          </div>
        </div>

        <div class="space-y-6">
          <div class="feature-item bg-white/10 backdrop-blur-sm rounded-lg p-6">
            <h3 class="text-xl font-semibold mb-2">Integration Features</h3>
            <p class="text-blue-200">Specify mounting points, shaft connections, and interfaces</p>
          </div>
          
          <div class="feature-item bg-white/10 backdrop-blur-sm rounded-lg p-6">
            <h3 class="text-xl font-semibold mb-2">Performance Parameters</h3>
            <p class="text-blue-200">Tell us your torque, speed, and duty cycle requirements</p>
          </div>
          
          <div class="text-center mt-8">
            <a href="#contact" 
               class="inline-block bg-white text-blue-900 font-semibold px-8 py-4 rounded-lg hover:bg-blue-50 transition-colors">
              Start Your Custom Design
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>