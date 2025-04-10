<script setup lang="ts">
import { onMounted } from 'vue';
import anime from 'animejs';

onMounted(() => {
  anime({
    targets: '.about-item',
    opacity: [0, 1],
    translateY: [20, 0],
    delay: anime.stagger(200),
    easing: 'easeOutQuad',
    duration: 800,
    threshold: 0.5
  });
});
</script>

<template>
  <section id="about" class="w-full py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl font-bold text-gray-900 mb-4">Our Story</h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Founded in Munich, Germany, WunderworkGmbH has been at the forefront of mechanical motion innovation for over two decades.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-12">
        <div class="about-item bg-white p-8 rounded-xl shadow-lg">
          <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Beginning</h3>
          <p class="text-gray-600">
            What began as a specialized engineering workshop has evolved into a global supplier of premium elliptical gears, serving industries where precision and reliability are non-negotiable.
          </p>
        </div>

        <div class="about-item bg-white p-8 rounded-xl shadow-lg">
          <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Approach</h3>
          <p class="text-gray-600">
            We combine traditional German engineering excellence with cutting-edge manufacturing technology. Our team of mechanical engineers and materials specialists work together to push the boundaries of what's possible.
          </p>
        </div>

        <div class="about-item bg-white p-8 rounded-xl shadow-lg">
          <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Commitment</h3>
          <p class="text-gray-600">
            Quality is embedded in every step of our process, from material selection to final testing. We maintain ISO 9001:2015 certification and adhere to the strictest industry standards.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>