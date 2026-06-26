<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

useHead({
    title: "Public Speaking | Philippe Gerwill",
    meta: [
        {
            name: "description",
            content:
                "Philippe Gerwill is an internationally recognized keynote speaker and panelist on AI, digital health, healthcare innovation, and the future of humanity.",
        },
    ],
});

const introParagraphs = [
    "I am an internationally recognized keynote speaker and panelist, regularly invited to address global audiences on the transformative impact of artificial intelligence, digital health, and emerging technologies. My speaking engagements span leading conferences, executive forums, academic institutions, and high-level industry events across Europe, the Middle East, Africa, and beyond. Known for my ability to translate complex technological concepts into clear, actionable insights, I bring a unique perspective that combines strategic foresight with real-world experience.",
    "My talks go beyond technology to explore the deeper implications of innovation on healthcare systems, business models, and society at large. With a strong emphasis on human-centered design, I challenge organizations to rethink how they adopt and scale innovation in a way that preserves empathy, ethics, and purpose.",
    "Whether delivering keynote presentations, moderating high-level panels, or participating in strategic discussions, I consistently engage audiences with thought-provoking narratives, practical examples, and a forward-looking vision of healthcare and longevity. Through my public speaking, I not only inform but inspire action, encouraging leaders, practitioners, and innovators to embrace change while ensuring that technology remains a tool to enhance, rather than replace, the human experience.",
];

const speakingEvents = [
    {
        title: "Game Changers Switzerland 2026",
        location: "Zurich, Switzerland",
        image: "/images/public-speaking/game-changers-switzerland-2026.webp",
    },
    {
        title: "Global Gaming Show 2025",
        location: "Abu Dhabi, UAE",
        image: "/images/public-speaking/global-gaming-show-2025.webp",
    },
    {
        title: "Global AI Show 2025",
        location: "Abu Dhabi, UAE",
        image: "/images/public-speaking/global-ai-show-2025.webp",
    },
    {
        title: "MedTech World 2025",
        location: "La Valetta, Malta",
        image: "/images/public-speaking/medtech-world-2025.webp",
    },
    {
        title: "Smart Health Africa 2025",
        location: "Pretoria, South Africa",
        image: "/images/public-speaking/smart-health-africa-2025.webp",
    },
    {
        title: "Arab Health 2025",
        location: "Dubai, UAE",
        image: "/images/public-speaking/arab-health-2025.webp",
    },
    {
        title: "Afya Summit 2024",
        location: "Sao Paulo, Brazil",
        image: "/images/public-speaking/afya-summit-2024.webp",
    },
    {
        title: "S-Tron China 2024",
        location: "Shanghai, China",
        image: "/images/public-speaking/s-tron-china-2024.webp",
    },
];
</script>

<template>
    <main class="bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <section class="py-14 sm:py-16 lg:py-20">
            <AppContainer>
                <div class="mx-auto max-w-6xl">
                    <div class="mx-auto max-w-4xl text-center">
                        <h1
                            class="text-[46px] font-[500] leading-none tracking-[-0.07em] text-[#4A1BC4] dark:text-[#C8EB00] sm:text-[60px] lg:text-[76px]">
                            Public Speaking
                        </h1>

                        <p
                            class="mx-auto mt-5 max-w-2xl text-[16px] font-[500] leading-[1.55] tracking-[-0.03em] text-black/65 dark:text-white/75 sm:text-[18px]">
                            Keynotes on AI, digital health, innovation, longevity, and the
                            future of human-centered healthcare.
                        </p>
                    </div>

                    <div class="mx-auto mt-12 max-w-5xl lg:mt-16">
                        <div class="grid gap-x-10 gap-y-12 rounded-[28px] p-6 sm:p-8 lg:grid-cols-2 lg:p-0">
                            <!-- First paragraph full width -->
                            <article class="relative lg:col-span-2">
                                <div class="mb-5 h-[4px] w-16 rounded-full bg-[#4A1BC4] dark:bg-[#C8EB00]"
                                    aria-hidden="true"></div>

                                <p
                                    class="max-w-5xl text-[16px] font-[500] leading-[1.8] tracking-[-0.035em] text-black dark:text-white sm:text-[17px] lg:text-[20px] lg:leading-[1.7]">
                                    {{ introParagraphs[0] }}
                                </p>
                            </article>

                            <!-- Second paragraph left -->
                            <article class="relative">
                                <div class="mb-5 h-[4px] w-16 rounded-full bg-[#4A1BC4] dark:bg-[#C8EB00]"
                                    aria-hidden="true"></div>

                                <p
                                    class="text-[16px] font-[500] leading-[1.8] tracking-[-0.035em] text-black dark:text-white sm:text-[17px] lg:text-[18px] lg:leading-[1.75]">
                                    {{ introParagraphs[1] }}
                                </p>
                            </article>

                            <!-- Third paragraph right -->
                            <article class="relative">
                                <div class="mb-5 h-[4px] w-16 rounded-full bg-[#4A1BC4] dark:bg-[#C8EB00]"
                                    aria-hidden="true"></div>

                                <p
                                    class="text-[16px] font-[500] leading-[1.8] tracking-[-0.035em] text-black dark:text-white sm:text-[17px] lg:text-[18px] lg:leading-[1.75]">
                                    {{ introParagraphs[2] }}
                                </p>
                            </article>
                        </div>
                    </div>
                </div>
            </AppContainer>
        </section>

        <section class="pb-16 sm:pb-20 lg:pb-24">
            <AppContainer>
                <div class="mx-auto max-w-6xl">
                    <div class="mb-8 flex flex-col gap-3 sm:mb-10 sm:flex-row sm:items-end sm:justify-between">
                        <div>
                            <p
                                class="text-[13px] font-[700] uppercase tracking-[0.24em] text-[#4A1BC4] dark:text-[#C8EB00]">
                                Selected Engagements
                            </p>

                            <h2
                                class="mt-3 text-[30px] font-[700] leading-tight tracking-[-0.04em] text-black dark:text-white sm:text-[40px]">
                                Speaking Highlights
                            </h2>
                        </div>
                    </div>

                    <div class="grid gap-5 sm:grid-cols-2 lg:grid-cols-4">
                        <article v-for="event in speakingEvents" :key="event.title"
                            class="group rounded-[22px] bg-black/[0.03] p-3 transition duration-300 hover:-translate-y-1 hover:bg-black/[0.05] dark:bg-[#101010] dark:hover:bg-[#181818]">
                            <div class="overflow-hidden rounded-[16px]">
                                <img :src="event.image" :alt="event.title"
                                    class="h-[340px] w-full object-cover object-center transition duration-500 group-hover:scale-[1.04] sm:h-[380px] lg:h-[360px]"
                                    loading="lazy" />
                            </div>

                            <div class="px-1 pb-2 pt-4">
                                <h3 class="text-[16px] font-[800] leading-tight text-[#4A1BC4] dark:text-[#C8EB00]">
                                    {{ event.title }}
                                </h3>

                                <p class="mt-2 text-[13px] font-[700] text-black/55 dark:text-white/60">
                                    {{ event.location }}
                                </p>
                            </div>
                        </article>
                    </div>
                </div>
            </AppContainer>
        </section>
    </main>
</template>