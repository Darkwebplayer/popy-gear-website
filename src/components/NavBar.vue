<script setup lang="ts">
import { ref } from 'vue';

const isMenuOpen = ref(false);

const menuItems = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Products', href: '#products' },
  { name: 'Customization', href: '#customization' },
  { name: 'Testimonials', href: '#testimonials' },
  { name: 'Contact', href: '#contact' }
];
</script>

<template>
  <nav class="fixed w-full bg-white/90 backdrop-blur-sm z-50 shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between h-16">
        <div class="flex items-center">
          <span class="text-xl font-bold text-gray-900">WunderworkGmbH</span>
        </div>
        
        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center space-x-8">
          <a v-for="item in menuItems" 
             :key="item.name" 
             :href="item.href"
             class="text-gray-700 hover:text-blue-600 transition-colors">
            {{ item.name }}
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <div class="md:hidden flex items-center">
          <button @click="isMenuOpen = !isMenuOpen" 
                  class="text-gray-700">
            <span class="sr-only">Open menu</span>
            <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
            </svg>
          </button>
        </div>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-show="isMenuOpen" class="md:hidden">
      <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
        <a v-for="item in menuItems" 
           :key="item.name" 
           :href="item.href"
           @click="isMenuOpen = false"
           class="block px-3 py-2 text-gray-700 hover:text-blue-600 transition-colors">
          {{ item.name }}
        </a>
      </div>
    </div>
  </nav>
</template>