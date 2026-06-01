<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

useHead({
    title: "Media & Publications | Philippe Gerwill",
    meta: [
        {
            name: "description",
            content:
                "Philippe Gerwill shares perspectives on artificial intelligence, digital health, longevity, and human-centered innovation across global media platforms.",
        },
    ],
});

const paragraphs = [
    "I am privileged to contribute regularly to international media platforms, industry publications, and podcasts, where I share my perspectives on artificial intelligence, digital health, and human-centered innovation. Through articles, interviews, and editorial contributions, I aim to actively shape the global conversation on the future of healthcare, longevity, and the responsible integration of emerging technologies.",
    "My writing reflects my commitment to bridging strategic foresight with practical relevance. Whether I address regulatory challenges, explore new healthcare paradigms, or highlight breakthrough innovations, my objective is always to bring clarity to complex topics while advocating for approaches that place people at the center of transformation. My perspectives are grounded in both my executive experience and my ongoing engagement with global ecosystems of innovators, policymakers, and healthcare leaders.",
    "Beyond traditional media, I leverage digital platforms to extend my reach and impact. Through my newsletters Healthcare in the Metaverse and Beyond the Algorithm, I share deeper reflections, frameworks, and forward-looking ideas with a growing international audience. In parallel, my participation in podcasts allows me to engage in more open, conversational discussions, making complex topics more accessible and fostering meaningful dialogue across disciplines and geographies.",
    "Through these various channels, my ambition is not only to inform but also to challenge assumptions, stimulate reflection, and inspire a more human-centered approach to technological progress in healthcare and beyond.",
];

const publications = [
    {
        title: "Conglomerate Magazine",
        image: "/images/media-publications/conglomerate-magazine.webp",
        href: "https://conglomeratemagazine.com/the-digital-humanist/",
    },
    {
        title: "Entrepreneur's Echo",
        image: "/images/media-publications/entrepreneurs-echo.webp",
        href: "https://entrepreneursecho.com/the-digital-humanist-how-philippe-gerwill-is-shaping-the-future-of-health-tech/",
    },
    {
        title: "Elite Business Chronicles",
        image: "/images/media-publications/elite-business-chronicles.webp",
        href: "https://elitebusinesschronicles.com/philippe-grewill-the-visionary-human-tech-integrator-shaping-tomorrows-healthcare-landscape-2026/",
    },
];
</script>

<template>
    <main class="bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <section class="py-14 sm:py-16 lg:py-20">
            <AppContainer>
                <div class="grid gap-12 lg:grid-cols-[0.9fr_1.1fr] lg:items-start lg:gap-16">
                    <div class="lg:sticky lg:top-28">
                        <p
                            class="text-[13px] font-[700] uppercase tracking-[0.22em] text-[#4A1BC4] dark:text-[#C8EB00]">
                            Media & Publications
                        </p>

                        <h1
                            class="mt-5 max-w-[620px] text-[46px] font-[500] uppercase leading-[0.92] tracking-[-0.08em] text-[#4A1BC4] dark:text-[#C8EB00] sm:text-[55px] lg:text-[60px]">
                            From Insight to Impact
                        </h1>

                        <p
                            class="mt-7 max-w-[560px] text-[20px] font-[500] leading-[1.25] tracking-[-0.04em] text-black/70 dark:text-white/75 sm:text-[20px]">
                            Across Global Media Platforms
                        </p>

                        <div class="mt-10 space-y-7">
                            <p v-for="(paragraph, index) in paragraphs" :key="index"
                                class="text-[17px] font-[500] leading-[1.75] tracking-[-0.035em] text-black dark:text-white sm:text-[18px]">
                                {{ paragraph }}
                            </p>
                        </div>
                    </div>

                    <div>
                        <div class="grid gap-6 sm:grid-cols-2">
                            <a v-for="(item, index) in publications" :key="item.title" :href="item.href" target="_blank"
                                rel="noopener noreferrer"
                                class="group block rounded-[18px] bg-[#EDEDED] p-4 transition duration-300 hover:-translate-y-1 dark:bg-[#101010]"
                                :class="index === 1 ? 'sm:col-span-2 sm:mx-auto sm:w-[58%] lg:w-[64%]' : ''"
                                :aria-label="item.title">
                                <div
                                    class="flex aspect-[3/4] items-center justify-center overflow-hidden rounded-[12px] bg-black">
                                    <img :src="item.image" :alt="item.title"
                                        class="h-full w-full object-contain object-center transition duration-500 group-hover:scale-[1.03]"
                                        loading="lazy" />
                                </div>

                                <div class="mt-4 flex items-center justify-between gap-4">
                                    <h2
                                        class="text-[15px] font-[700] leading-tight tracking-[-0.04em] text-black dark:text-white">
                                        {{ item.title }}
                                    </h2>

                                    <span
                                        class="inline-flex size-9 shrink-0 items-center justify-center rounded-full bg-[#C8EB00] text-black transition duration-300 group-hover:rotate-45"
                                        aria-hidden="true">
                                        <svg xmlns="http://www.w3.org/2000/svg" class="size-4" viewBox="0 0 24 24"
                                            fill="none" stroke="currentColor" stroke-width="2">
                                            <path d="M7 17 17 7" />
                                            <path d="M7 7h10v10" />
                                        </svg>
                                    </span>
                                </div>
                            </a>
                        </div>
                    </div>
                </div>
            </AppContainer>
        </section>
    </main>
</template>