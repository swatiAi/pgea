<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";
import UiButton from "~/components/ui/Button.vue";

const hero = {
    title: "I’m Philippe Gerwill",
    description:
        "Hi There! I’m An International Speaker, A Key Opinion Leader, An Advisor & Board Member Bridging Artificial Intelligence, Healthcare, And Humanity On A Global Stage",
    image: "/images/philippe-hero.webp",
};
</script>

<template>
    <section class="relative min-h-[calc(100vh-94px)] overflow-hidden border-b border-[#4A1BC4] bg-black text-white">
        <img :src="hero.image" alt="Philippe Gerwill speaking on stage"
            class="absolute inset-0 size-full object-cover object-[62%_center] sm:object-[64%_center] md:object-[68%_center] lg:object-center" />

        <div
            class="absolute inset-0 bg-gradient-to-r from-black/75 via-black/40 to-black/10 md:from-black/70 md:via-black/35 md:to-black/5 lg:bg-black/20">
        </div>

        <AppContainer>
            <div
                class="relative z-10 flex min-h-[calc(100vh-94px)] max-w-[620px] flex-col justify-center py-16 sm:py-20">
                <h1
                    class="max-w-[520px] text-[46px] font-[500] uppercase leading-[0.96] tracking-[-0.06em] text-[#C8EB00] sm:text-[58px] md:text-[68px] lg:text-[76px]">
                    {{ hero.title }}
                </h1>

                <p
                    class="mt-6 max-w-[500px] text-[15px] font-[500] leading-[1.08] tracking-[-0.04em] text-white sm:text-[16px] md:mt-7 md:text-[17px]">
                    {{ hero.description }}
                </p>

                <div class="mt-9 sm:mt-10">
                    <UiButton href="https://pgerwill.com/wp-content/uploads/2026/04/PGEA-Positioning.pdf" variant="hero"
                        size="lg"
                        class="min-h-[64px] min-w-[250px] px-8 text-[18px] tracking-[-0.04em] sm:min-h-[72px] sm:min-w-[280px] sm:px-9 sm:text-[21px]">
                        <svg xmlns="http://www.w3.org/2000/svg" class="size-5" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2">
                            <path d="M12 3v12" />
                            <path d="m7 10 5 5 5-5" />
                            <path d="M5 21h14" />
                        </svg>

                        Download Services
                    </UiButton>
                </div>
            </div>
        </AppContainer>
    </section>
</template>