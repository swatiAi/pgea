<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";
import UiButton from "~/components/ui/Button.vue";

const about = {
    text: "Philippe is an internationally recognized Digital Health Futurist, Innovation Strategist, and Key Opinion Leader, operating at the intersection of artificial intelligence, longevity, and human-centric healthcare.",
    lightImage: "/images/philippe-about-light.webp",
    darkImage: "/images/about-dark.webp",
};
</script>

<template>
    <section class="overflow-hidden bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <AppContainer>
            <div
                class="grid min-h-[520px] items-center gap-12 py-14 md:min-h-[560px] md:grid-cols-2 md:gap-14 lg:min-h-[620px] lg:gap-20 lg:py-20">
                <div class="mx-auto max-w-[560px] text-center md:mx-0 md:text-left">
                    <p class="text-[23px] font-[500] leading-[1.12] tracking-[-0.045em] sm:text-[26px] lg:text-[28px]">
                        {{ about.text }}
                    </p>

                    <div class="mt-9 flex justify-center md:mt-12 md:justify-start">
                        <UiButton to="/about" size="lg"
                            class="min-h-[64px] min-w-[220px] px-10 text-[18px] font-[400] tracking-[-0.04em] sm:min-h-[72px] sm:min-w-[240px] sm:text-[20px]">
                            Know More
                        </UiButton>
                    </div>
                </div>

                <div class="relative flex min-h-[320px] items-center justify-center sm:min-h-[420px] md:min-h-[480px]">
                    <div
                        class="flex h-[340px] w-full max-w-[430px] items-center justify-end overflow-hidden rounded-[10px] bg-[#eeeeea] sm:h-[460px] sm:max-w-none md:h-[520px] dark:hidden">
                        <img :src="about.lightImage" alt="Philippe Gerwill portrait"
                            class="h-full w-full object-cover object-center" />
                    </div>


                    <div class="hidden w-full items-center justify-center dark:flex">
                        <img :src="about.darkImage" alt="Philippe Gerwill portrait with geometric background"
                            class="w-full max-w-[360px] object-contain sm:max-w-[500px] md:max-w-[560px] lg:max-w-[640px]" />
                    </div>
                </div>
            </div>
        </AppContainer>
    </section>
</template>