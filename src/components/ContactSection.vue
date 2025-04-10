<script setup lang="ts">
import { onMounted } from 'vue';
import anime from 'animejs';

onMounted(() => {
  anime({
    targets: '.contact-item',
    translateY: [20, 0],
    opacity: [0, 1],
    delay: anime.stagger(100),
    duration: 800,
    easing: 'easeOutQuad'
  });
});
</script>

<template>
  <section id="contact" class="w-full py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="max-w-3xl mx-auto text-center">
        <h2 class="text-4xl font-bold text-gray-900 mb-6">Get in Touch</h2>
        <p class="text-xl text-gray-600 mb-12">
          Ready to discuss your elliptical gear needs? Our engineering team is available to consult on your specific application requirements.
        </p>
        
        <div class="space-y-8">
          <div class="contact-item bg-gray-50 p-8 rounded-xl shadow-lg">
            <h3 class="text-2xl font-semibold text-gray-900 mb-4">Contact Information</h3>
            <div class="space-y-3">
              <p class="text-gray-600 flex items-center justify-center">
                <svg class="w-6 h-6 mr-3 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                </svg>
                info@wunderworkgmbh.com
              </p>
              <p class="text-gray-600 flex items-center justify-center">
                <svg class="w-6 h-6 mr-3 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                </svg>
                +49 (0) 89 1234 5678
              </p>
              <p class="text-gray-600 flex items-center justify-center">
                <svg class="w-6 h-6 mr-3 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                Industriestraße 45, 80939 Munich, Germany
              </p>
            </div>
          </div>
          
          <div class="contact-item bg-gray-50 p-8 rounded-xl shadow-lg">
            <h3 class="text-2xl font-semibold text-gray-900 mb-4">Office Hours</h3>
            <p class="text-gray-600 flex items-center justify-center">
              <svg class="w-6 h-6 mr-3 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
              </svg>
              Monday-Friday: 8:00 AM - 5:00 PM CET
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>