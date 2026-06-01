<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

const stats = [
    {
        value: 35,
        suffix: "+",
        label: "Years Of Global Leadership",
    },
    {
        value: 50,
        suffix: "+",
        label: "Countries Engaged",
    },
    {
        value: 30,
        suffix: "+",
        label: "Advisory & Board Roles",
    },
    {
        value: 150,
        suffix: "K+",
        label: "Global Community",
    },
];

const sectionRef = ref(null);
const hasAnimated = ref(false);
const counts = ref(stats.map(() => 0));

const animateCounts = () => {
    if (hasAnimated.value) return;

    hasAnimated.value = true;

    stats.forEach((item, index) => {
        const duration = 1400;
        const startTime = performance.now();

        const updateCount = (currentTime) => {
            const progress = Math.min((currentTime - startTime) / duration, 1);
            const easedProgress = 1 - Math.pow(1 - progress, 3);

            counts.value[index] = Math.floor(item.value * easedProgress);

            if (progress < 1) {
                requestAnimationFrame(updateCount);
            } else {
                counts.value[index] = item.value;
            }
        };

        requestAnimationFrame(updateCount);
    });
};

onMounted(() => {
    const observer = new IntersectionObserver(
        ([entry]) => {
            if (entry.isIntersecting) {
                animateCounts();
                observer.disconnect();
            }
        },
        {
            threshold: 0.25,
        },
    );

    if (sectionRef.value) {
        observer.observe(sectionRef.value);
    }
});
</script>

<template>
    <section ref="sectionRef" class="bg-[#4A1BC4] text-[#C8EB00]">
        <AppContainer>
            <div class="mx-auto flex min-h-[170px] w-full max-w-6xl items-center py-10">
                <div class="grid w-full grid-cols-2 gap-y-10 lg:grid-cols-4 lg:gap-y-0">
                    <div v-for="(item, index) in stats" :key="item.label"
                        class="relative flex w-full items-center justify-center px-3 text-center">
                        <div v-if="index !== 0"
                            class="absolute left-0 top-1/2 hidden h-[84px] w-px -translate-y-1/2 bg-[#C8EB00]/70 lg:block">
                        </div>

                        <div class="flex w-full translate-y-3 flex-col items-center justify-center opacity-0 animate-[statFadeUp_700ms_ease-out_forwards]"
                            :style="{ animationDelay: `${index * 120}ms` }">
                            <p
                                class="text-center text-[52px] font-[400] leading-none tracking-[-0.07em] sm:text-[60px] lg:text-[68px]">
                                {{ counts[index] }}{{ item.suffix }}
                            </p>

                            <p
                                class="mt-3 max-w-[150px] text-center text-[10px] font-[700] leading-[1.1] tracking-[-0.03em] sm:max-w-none sm:text-[12px]">
                                {{ item.label }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </AppContainer>
    </section>
</template>

<style>
@keyframes statFadeUp {
    from {
        opacity: 0;
        transform: translateY(12px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}
</style>