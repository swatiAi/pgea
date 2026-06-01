<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

const testimonials = [
    {
        text: `We had the absolute privilege of hosting Philippe as a keynote speaker at the 2025 Smart Health Africa Summit, and he was a joy to work with. His presentation on the future of healthcare was not only insightful but also delivered a deep sense of passion for the industry.

Beyond the stage, Philippe was an absolute gentleman - professional, approachable, and a joy to work with throughout the entire process. From preparation to delivery, he made the experience seamless for our team.

We couldn’t recommend Philippe highly enough as both a thought leader and a collaborative partner.`,
        name: "Kelly Bentley",
        role: "The Rebel Element",
        avatar: "/images/kelly-bentley.webp",
    },
    {
        text: `We had the absolute privilege of hosting Philippe as a keynote speaker at the 2025 Smart Health Africa Summit, and he was a joy to work with. His presentation on the future of healthcare was not only insightful but also delivered a deep sense of passion for the industry.

Beyond the stage, Philippe was an absolute gentleman - professional, approachable, and a joy to work with throughout the entire process. From preparation to delivery, he made the experience seamless for our team.

We couldn’t recommend Philippe highly enough as both a thought leader and a collaborative partner.`,
        name: "Kelly Bentley",
        role: "The Rebel Element",
        avatar: "/images/kelly-bentley.webp",
    },
    {
        text: `We had the absolute privilege of hosting Philippe as a keynote speaker at the 2025 Smart Health Africa Summit, and he was a joy to work with. His presentation on the future of healthcare was not only insightful but also delivered a deep sense of passion for the industry.

Beyond the stage, Philippe was an absolute gentleman - professional, approachable, and a joy to work with throughout the entire process. From preparation to delivery, he made the experience seamless for our team.

We couldn’t recommend Philippe highly enough as both a thought leader and a collaborative partner.`,
        name: "Kelly Bentley",
        role: "The Rebel Element",
        avatar: "/images/kelly-bentley.webp",
    },
];
</script>

<template>
    <section class="bg-white py-16 text-black transition-colors duration-200 dark:bg-black dark:text-white lg:py-24">
        <AppContainer>
            <h2
                class="text-center text-[36px] font-[500] leading-none tracking-[-0.06em] sm:text-[44px] lg:text-[52px]">
                Testimonials
            </h2>

            <div class="mt-12 grid gap-8 md:grid-cols-3 lg:mt-16">
                <article v-for="(item, index) in testimonials" :key="index"
                    class="group flex min-h-[430px] flex-col justify-between rounded-[6px] bg-gradient-to-b from-white via-[#FBFFE8] to-[#E8FF65] px-8 py-7 text-black shadow-sm transition duration-300 hover:-translate-y-1 sm:min-h-[460px] lg:min-h-[500px] lg:px-9 lg:py-8">
                    <div>
                        <span class="block text-[76px] font-[900] leading-[0.6] tracking-[-0.08em] text-black">
                            “
                        </span>

                        <p
                            class="mt-5 whitespace-pre-line text-[14px] font-[400] leading-[1.14] tracking-[-0.035em] lg:text-[15px]">
                            {{ item.text }}
                        </p>
                    </div>

                    <div class="mt-8 flex items-center gap-3">
                        <img :src="item.avatar" :alt="item.name" class="size-8 rounded-full object-cover" />

                        <div>
                            <h3 class="text-[12px] font-[800] leading-none tracking-[-0.03em] text-black">
                                {{ item.name }}
                            </h3>

                            <p class="mt-1 text-[12px] font-[700] leading-none tracking-[-0.03em] text-black">
                                {{ item.role }}
                            </p>
                        </div>
                    </div>
                </article>
            </div>
        </AppContainer>
    </section>
</template>