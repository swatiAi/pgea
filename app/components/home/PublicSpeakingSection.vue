<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

const events = [
    {
        title: "Game Changers Switzerland 2026",
        location: "Zurich, Switzerland",
        image: "/images/game-changers.webp",
        badgeClass: "bg-[#C8EB00] text-black",
    },
    {
        title: "Smart Health Africa 2025",
        location: "Pretoria, South Africa",
        image: "/images/smart-health.webp",
        badgeClass: "bg-[#4A1BC4] text-white",
    },
    {
        title: "Arab Health 2025",
        location: "Dubai, UAE",
        image: "/images/arab-health.webp",
        badgeClass: "bg-[#C8EB00] text-black",
    },
];
</script>

<template>
    <section class="bg-[#EDEDED] py-14 text-black dark:bg-white lg:py-20">
        <AppContainer>
            <div class="mb-10 grid gap-6 md:grid-cols-[1fr_auto] md:items-start">
                <div>
                    <h2 class="text-[52px] font-[500] leading-none tracking-[-0.07em] sm:text-[64px] lg:text-[78px]">
                        Public Speaking
                    </h2>

                    <div class="mt-5 h-[3px] w-[145px] bg-[#4A1BC4]"></div>
                </div>

                <p class="max-w-[260px] text-[17px] font-[400] leading-[1.1] tracking-[-0.04em] md:pt-4">
                    Keynotes on AI, Health, and the Future of Humanity
                </p>
            </div>

            <div class="grid gap-6 md:grid-cols-3 lg:gap-8">
                <article v-for="event in events" :key="event.title"
                    class="group relative min-h-[360px] overflow-hidden rounded-[4px] bg-white sm:min-h-[430px] lg:min-h-[460px]">
                    <img :src="event.image" :alt="event.title"
                        class="absolute inset-0 size-full object-cover transition duration-500 group-hover:scale-105" />

                    <div class="absolute bottom-0 left-0 min-h-[92px] w-[150px] p-4 sm:w-[170px] lg:w-[190px]"
                        :class="event.badgeClass">
                        <h3 class="text-[15px] font-[700] leading-[1.05] tracking-[-0.04em] sm:text-[17px]">
                            {{ event.title }}
                        </h3>

                        <p class="mt-2 text-[8px] font-[400] leading-none tracking-[-0.03em] opacity-90 sm:text-[12px]">
                            {{ event.location }}
                        </p>
                    </div>
                </article>
            </div>
        </AppContainer>
    </section>
</template>