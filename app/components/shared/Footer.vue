<script setup>
import AppContainer from "~/components/ui/AppContainer.vue";

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

const socialLinks = [
    {
        label: "LinkedIn",
        href: "https://www.linkedin.com/in/philippegerwill/",
    },
    {
        label: "Instagram",
        href: "https://www.instagram.com/pgerwill/",
    },
    {
        label: "Twitter/X",
        href: "https://x.com/pgerwill",
    },
    {
        label: "Facebook",
        href: "https://www.facebook.com/philippe.gerwill",
    },
];

const socialIcons = [
    {
        label: "Facebook",
        href: "https://www.facebook.com/philippe.gerwill",
        icon: "/icons/facebook.svg",
    },
    {
        label: "Instagram",
        href: "https://www.instagram.com/pgerwill/",
        icon: "/icons/instagram.svg",
    },
    {
        label: "Twitter/X",
        href: "https://x.com/pgerwill",
        icon: "/icons/x.svg",
    },
    {
        label: "LinkedIn",
        href: "https://www.linkedin.com/in/philippegerwill/",
        icon: "/icons/linkedin.svg",
    },
];
</script>

<template>
    <footer class="bg-white text-black transition-colors duration-200 dark:bg-black dark:text-white">
        <AppContainer>
            <div
                class="grid gap-12 border-t border-black/10 py-12 dark:border-white/10 md:grid-cols-[1.45fr_0.55fr_0.55fr] md:gap-16 lg:py-16">
                <div>
                    <NuxtLink to="/" aria-label="Philippe Gerwill Home" class="inline-flex items-center gap-3">
                        <span class="relative inline-flex size-12 shrink-0 items-center justify-center sm:size-14">
                            <img src="/images/logo-light.webp" alt="" class="size-full object-contain dark:hidden" />

                            <img src="/images/logo-dark.webp" alt=""
                                class="hidden size-full object-contain dark:block" />
                        </span>

                        <span
                            class="flex flex-col text-[28px] font-[500] uppercase leading-[0.86] tracking-[-0.08em] text-[#4A1BC4] transition-colors duration-200 dark:text-[#C8EB00]">
                            <span>Philippe</span>
                            <span>Gerwill</span>
                        </span>
                    </NuxtLink>

                    <form class="mt-8 flex max-w-[560px] gap-3 max-sm:flex-col">
                        <label for="footer-email" class="sr-only">
                            Email address
                        </label>

                        <div class="relative flex-1">
                            <img src="/icons/mail.svg" alt=""
                                class="pointer-events-none absolute left-5 top-1/2 size-4 -translate-y-1/2" />

                            <input id="footer-email" type="email" placeholder="Email Here"
                                class="h-14 w-full rounded-[4px] bg-[#EDEDED] px-12 text-sm text-black outline-none placeholder:text-black/35 dark:bg-white" />
                        </div>

                        <button type="submit"
                            class="h-14 rounded-[4px] bg-[#C8EB00] px-8 text-[18px] font-[400] tracking-[-0.04em] text-black transition hover:opacity-90">
                            Subscribe
                        </button>
                    </form>

                    <div class="mt-8 flex items-center gap-4">
                        <a v-for="item in socialIcons" :key="item.label" :href="item.href" target="_blank"
                            rel="noopener noreferrer" :aria-label="item.label"
                            class="inline-flex size-4 items-center justify-center transition hover:opacity-75">
                            <img :src="item.icon" :alt="item.label" class="size-4 object-contain" />
                        </a>
                    </div>
                </div>

                <nav class="flex flex-col gap-3">
                    <NuxtLink v-for="link in navLinks" :key="link.to" :to="link.to"
                        class="text-[13px] font-[700] uppercase leading-none tracking-[-0.02em] transition hover:text-[#4A1BC4] dark:hover:text-[#C8EB00]">
                        {{ link.label }}
                    </NuxtLink>
                </nav>

                <nav class="flex flex-col gap-4">
                    <a v-for="link in socialLinks" :key="link.label" :href="link.href" target="_blank"
                        rel="noopener noreferrer"
                        class="text-[13px] font-[700] uppercase leading-none tracking-[-0.02em] transition hover:text-[#4A1BC4] dark:hover:text-[#C8EB00]">
                        {{ link.label }}
                    </a>
                </nav>
            </div>
        </AppContainer>
    </footer>
</template>