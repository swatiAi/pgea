<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

useHead({
    title: "About | Philippe Gerwill",
    meta: [
        {
            name: "description",
            content:
                "Philippe Gerwill is an internationally recognized Digital Health Futurist, Innovation Strategist, and Key Opinion Leader.",
        },
    ],
});

const firstParagraphStart = "Philippe is an internationally recognized ";

const firstParagraphBold =
    "Digital Health Futurist, Innovation Strategist, and Key Opinion Leader";

const firstParagraphEnd =
    ", operating at the intersection of artificial intelligence, longevity, and human-centric healthcare. With over 30 years of global experience across leading organizations such as Novartis, Lonza, and Ciba Specialty Chemicals, he brings a unique blend of strategic insight and real-world expertise. Today, as Founder and CEO of PGEA Ltd and a trusted advisor to governments, institutions, and startups, he supports organizations navigating the transformation of healthcare in an increasingly complex and technology-driven world.";

const secondParagraph =
    "A sought-after international keynote speaker and Adjunct Professor at the Rome Business School, Philippe is known for translating complex innovations into actionable, human-centered strategies. He is the creator of the “Longevity GPS” concept, a forward-looking approach that leverages AI, data, and digital twins to shift healthcare from reactive treatment to proactive life navigation. Guided by a strong belief that technology must serve humanity, he advocates for ethical, inclusive, and impactful innovation that places people, not technology at the center of healthcare’s future.";
</script>

<template>
    <main class="bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <section class="py-12 sm:py-16 lg:py-20">
            <AppContainer>
                <div class="mx-auto max-w-6xl">
                    <h1
                        class="text-center text-[48px] font-[500] leading-none tracking-[-0.07em] text-[#4A1BC4] dark:text-[#C8EB00] sm:text-[64px] lg:text-[76px]">
                        About
                    </h1>

                    <div class="mt-10 lg:mt-14">
                        <div class="grid gap-6 md:grid-cols-2 md:items-center lg:gap-10">
                            <div class="overflow-hidden rounded-[10px]">
                                <img src="/images/about/about-page.webp" alt="Philippe Gerwill"
                                    class="h-[360px] w-full object-cover object-top sm:h-[420px] md:h-[460px] lg:h-[500px]" />
                            </div>

                            <div class="flex items-center">
                                <p
                                    class="max-w-[540px] text-[18px] font-[400] leading-[1.42] tracking-[-0.04em] text-black/85 dark:text-white/85 sm:text-[20px] lg:text-[23px]">
                                    {{ firstParagraphStart }}
                                    <strong class="font-[700] text-black dark:text-white">
                                        {{ firstParagraphBold }}
                                    </strong>
                                    {{ firstParagraphEnd }}
                                </p>
                            </div>
                        </div>

                        <p
                            class="mt-7 w-full text-[18px] font-[400] leading-[1.42] tracking-[-0.04em] text-black/85 dark:text-white/85 sm:text-[20px] lg:mt-10 lg:text-[23px]">
                            {{ secondParagraph }}
                        </p>
                    </div>
                </div>
            </AppContainer>
        </section>
    </main>
</template>