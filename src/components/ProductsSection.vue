<script setup lang="ts">
import { onMounted } from "vue";
import anime from "animejs";

onMounted(() => {
    anime({
        targets: ".product-card",
        scale: [0.9, 1],
        opacity: [0, 1],
        delay: anime.stagger(150),
        duration: 800,
        easing: "easeOutElastic(1, .8)",
    });
});
</script>

<template>
    <section id="products" class="w-full py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center mb-16">
                <h2 class="text-4xl font-bold text-gray-900 mb-4">
                    Our Products
                </h2>
                <p class="text-xl text-gray-600 max-w-3xl mx-auto">
                    Discover our range of precision-engineered elliptical gears
                    designed for various applications
                </p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div
                    class="product-card bg-gray-50 rounded-2xl p-8 shadow-lg transform hover:scale-105 transition-transform duration-300"
                >
                    <div
                        class="h-48 overflow-hidden bg-gradient-to-br from-blue-500 to-blue-700 rounded-xl mb-6 flex items-center justify-center"
                    >
                        <div class="gear">
                            <img src="/gear1.jpeg" alt="desing 1" />
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">
                        Standard Elliptical Gears
                    </h3>
                    <p class="text-gray-600 mb-6">
                        Our catalog includes a comprehensive range of standard
                        elliptical gears in various sizes, materials, and
                        specifications.
                    </p>
                    <a
                        href="#contact"
                        class="text-blue-600 font-semibold hover:text-blue-800"
                        >Learn More →</a
                    >
                </div>

                <div
                    class="product-card bg-gray-50 rounded-2xl p-8 shadow-lg transform hover:scale-105 transition-transform duration-300"
                >
                    <div
                        class="h-48 overflow-hidden bg-gradient-to-br from-purple-500 to-purple-700 rounded-xl mb-6 flex items-center justify-center"
                    >
                        <div class="gear">
                             <img src="/gear2.jpeg" alt="desing 1"
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">
                        Semi-Custom Solutions
                    </h3>
                    <p class="text-gray-600 mb-6">
                        Need something specific? Our semi-custom options allow
                        you to select from our modifiable templates.
                    </p>
                    <a
                        href="#contact"
                        class="text-blue-600 font-semibold hover:text-blue-800"
                        >Learn More →</a
                    >
                </div>

                <div
                    class="product-card bg-gray-50 rounded-2xl p-8 shadow-lg transform hover:scale-105 transition-transform duration-300"
                >
                    <div
                        class="h-48 overflow-hidden bg-gradient-to-br from-indigo-500 to-indigo-700 rounded-xl mb-6 flex items-center justify-center"
                    >
                        <div class="gear">
                             <img src="/gear3.jpeg" alt="desing 1"
                        </div>
                    </div>
                    <h3 class="text-2xl font-bold text-gray-900 mb-4">
                        High-Performance Series
                    </h3>
                    <p class="text-gray-600 mb-6">
                        For applications where failure is not an option, our
                        High-Performance series offers enhanced durability.
                    </p>
                    <a
                        href="#contact"
                        class="text-blue-600 font-semibold hover:text-blue-800"
                        >Learn More →</a
                    >
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.gear {
    background: url("/gear.svg") no-repeat center;
    background-size: contain;
    opacity: 0.8;
}
</style>
