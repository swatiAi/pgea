<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";
import UiButton from "~/components/ui/Button.vue";
import ThemeToggle from "~/components/ui/ThemeToggle.vue";

const route = useRoute();

const isMenuOpen = ref(false);

const navLinks = [
    {
        label: "Home",
        to: "/",
    },
    {
        label: "About",
        to: "/about",
    },
    {
        label: "Public Speaking",
        to: "/public-speaking",
    },
    {
        label: "Advisory & Board Roles",
        to: "/advisory-board-roles",
    },
    {
        label: "Media & Publications",
        to: "/media-publications",
    },
];

const closeMenu = () => {
    isMenuOpen.value = false;
};

watch(
    () => route.fullPath,
    () => {
        closeMenu();
    },
);
</script>

<template>
    <header
        class="sticky top-0 z-50 border-b border-black/10 bg-white/95 text-black backdrop-blur transition-colors duration-200 dark:border-white/10 dark:bg-black/95 dark:text-white">
        <AppContainer>
            <nav class="flex h-[94px] items-center justify-between gap-5">
                <NuxtLink to="/" aria-label="Philippe Gerwill Home"
                    class="flex shrink-0 flex-col text-[24px] font-[500] uppercase leading-[0.86] tracking-[-0.08em] text-[#4A1BC4] transition-colors duration-200 dark:text-[#C8EB00] sm:text-[26px]"
                    @click="closeMenu">
                    <span>Philippe</span>
                    <span>Gerwill</span>
                </NuxtLink>

                <div class="hidden items-center gap-8 lg:flex xl:gap-12">
                    <NuxtLink v-for="link in navLinks" :key="link.to" :to="link.to"
                        class="text-[12px] font-[700] uppercase tracking-[-0.02em] text-black transition-colors duration-200 hover:text-[#4A1BC4] dark:text-white dark:hover:text-[#C8EB00] xl:text-[14px]"
                        active-class="!text-[#4A1BC4] dark:!text-[#C8EB00]">
                        {{ link.label }}
                    </NuxtLink>
                </div>

                <div class="flex shrink-0 items-center gap-3">
                    <UiButton href="mailto:philippe@pgerwill.com" size="md" class="hidden min-w-[130px] sm:inline-flex">
                        Contact Me
                    </UiButton>

                    <ThemeToggle />

                    <button type="button"
                        class="inline-flex size-10 items-center justify-center rounded-full border border-black/15 text-black transition hover:bg-black/5 dark:border-white/20 dark:text-white dark:hover:bg-white/10 lg:hidden"
                        :aria-label="isMenuOpen ? 'Close menu' : 'Open menu'" :aria-expanded="isMenuOpen"
                        @click="isMenuOpen = !isMenuOpen">
                        <svg v-if="!isMenuOpen" xmlns="http://www.w3.org/2000/svg" class="size-5" viewBox="0 0 24 24"
                            fill="none" stroke="currentColor" stroke-width="2">
                            <path d="M4 7h16" />
                            <path d="M4 12h16" />
                            <path d="M4 17h16" />
                        </svg>

                        <svg v-else xmlns="http://www.w3.org/2000/svg" class="size-5" viewBox="0 0 24 24" fill="none"
                            stroke="currentColor" stroke-width="2">
                            <path d="M6 6l12 12" />
                            <path d="M18 6 6 18" />
                        </svg>
                    </button>
                </div>
            </nav>

            <div class="grid overflow-hidden transition-[grid-template-rows] duration-300 lg:hidden"
                :class="isMenuOpen ? 'grid-rows-[1fr]' : 'grid-rows-[0fr]'">
                <div class="min-h-0">
                    <div class="border-t border-black/10 py-5 dark:border-white/10">
                        <div class="flex flex-col gap-1">
                            <NuxtLink v-for="link in navLinks" :key="link.to" :to="link.to"
                                class="rounded-xl px-4 py-3 text-[14px] font-[700] uppercase tracking-[-0.02em] text-black transition-colors duration-200 hover:bg-black/5 hover:text-[#4A1BC4] dark:text-white dark:hover:bg-white/10 dark:hover:text-[#C8EB00]"
                                active-class="!text-[#4A1BC4] dark:!text-[#C8EB00]" @click="closeMenu">
                                {{ link.label }}
                            </NuxtLink>

                            <UiButton href="mailto:philippe@pgerwill.com" size="md" class="mt-4 inline-flex w-full">
                                Contact Me
                            </UiButton>
                        </div>
                    </div>
                </div>
            </div>
        </AppContainer>
    </header>
</template>