<script setup lang="ts">
import { onMounted, ref } from "vue";
import anime from "animejs";
import gearSvgUrl from "@/assets/gear.svg";

const gearCanvas = ref<HTMLDivElement | null>(null); // Correct type hint

onMounted(() => {
    if (gearCanvas.value) {
        // Create animated gears
        const gears = Array.from({ length: 5 }).map((_, i) => {
            const gear = document.createElement("div");
            const gearSvg = document.createElement("img");
            gearSvg.src = gearSvgUrl;
            gearSvg.className = "gear-svg";
            gear.appendChild(gearSvg);
            gear.className = "absolute gear"; // Keep class 'absolute' for positioning if needed by anime/logic
            gear.style.width = `${80 + i * 20}px`;
            gear.style.height = `${80 + i * 20}px`;
            // Ensure positions don't make gears go completely off-screen initially
            gear.style.left = `${Math.random() * (gearCanvas.value?.clientWidth || window.innerWidth) * 0.7}px`; // Position relative to container width
            gear.style.top = `${Math.random() * (gearCanvas.value?.clientHeight || window.innerHeight) * 0.7}px`; // Position relative to container height
            gearCanvas.value?.appendChild(gear);
            return gear;
        });

        // Animate gears
        anime({
            targets: gears,
            rotate: "360deg",
            duration: 8000,
            loop: true,
            easing: "linear",
            delay: anime.stagger(200),
        });
    }
});
</script>

<template>
    <section
        id="home"
        class="md:py-0 py-32 relative min-h-screen flex items-center justify-center bg-gradient-to-br from-gray-900 to-blue-900 overflow-hidden"
    >
        <!-- This div is the container for the dynamically generated gears -->
        <!-- It controls the overall opacity of the background animation -->
        <div
            ref="gearCanvas"
            class="absolute inset-0 opacity-20 pointer-events-none"
            :style="{ '--gear-image-url': `url(${gearSvgUrl})` }"
        >
            <!-- REMOVED the static <img src="/gear.svg" /> -->
            <!-- Gears are added here dynamically by the script -->
        </div>

        <div class="relative z-10 max-w-4xl mx-auto text-center px-4">
            <h1 class="text-5xl md:text-6xl font-bold text-white mb-6">
                Precision Engineering for Motion Innovation
            </h1>
            <p class="text-xl md:text-2xl text-gray-300 mb-8">
                Turning Perfection Into Motion
            </p>
            <p class="text-lg text-gray-300 mb-12 max-w-2xl mx-auto">
                Welcome to WunderworkGmbH, the industry leader in
                precision-engineered elliptical gears. Our specialized
                manufacturing processes deliver unmatched quality and
                performance.
            </p>
            <a
                href="#customization"
                class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold px-8 py-4 rounded-lg transition-colors"
            >
                Design Your Custom Gear
            </a>
        </div>
    </section>
</template>

<style scoped>
.gear {
    /* 3. Use the CSS variable for the background image */
    background-image: var(--gear-image-url);
    background-repeat: no-repeat;
    background-position: center center;
    background-size: contain;
    will-change: transform;
    /* Opacity is handled by the parent 'gearCanvas' div */
}
</style>
