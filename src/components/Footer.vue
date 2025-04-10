<script setup lang="ts">
const currentYear = new Date().getFullYear();
</script>

<template>
  <footer class="w-full bg-gray-900 text-white py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <div>
          <h3 class="text-lg font-semibold mb-4">WunderworkGmbH</h3>
          <p class="text-gray-400">
            Precision engineering for motion innovation since 2000.
          </p>
        </div>
        
        <div>
          <h3 class="text-lg font-semibold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li><a href="#home" class="text-gray-400 hover:text-white transition-colors">Home</a></li>
            <li><a href="#about" class="text-gray-400 hover:text-white transition-colors">About</a></li>
            <li><a href="#products" class="text-gray-400 hover:text-white transition-colors">Products</a></li>
            <li><a href="#customization" class="text-gray-400 hover:text-white transition-colors">Customization</a></li>
          </ul>
        </div>
        
        <div>
          <h3 class="text-lg font-semibold mb-4">Contact</h3>
          <ul class="space-y-2 text-gray-400">
            <li>Munich, Germany</li>
            <li>+49 (0) 89 1234 5678</li>
            <li>info@wunderworkgmbh.com</li>
          </ul>
        </div>
        
        <div>
          <h3 class="text-lg font-semibold mb-4">Certifications</h3>
          <ul class="space-y-2 text-gray-400">
            <li>ISO 9001:2015</li>
            <li>DIN EN ISO 14001</li>
            <li>IATF 16949</li>
          </ul>
        </div>
      </div>
      
      <div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
        <p>&copy; {{ currentYear }} WunderworkGmbH. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>