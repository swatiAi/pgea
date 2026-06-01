<script setup>
import Navbar from "~/components/shared/Navbar.vue";
import Footer from "~/components/shared/Footer.vue";
</script>

<template>
    <div class="min-h-screen bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <Navbar />

        <main>
            <slot />
        </main>

        <Footer />
    </div>
</template>