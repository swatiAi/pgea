<script setup>
const isDark = useState("is-dark-mode", () => false);

const applyTheme = () => {
    if (!import.meta.client) return;

    document.documentElement.classList.toggle("dark", isDark.value);
    localStorage.setItem("theme", isDark.value ? "dark" : "light");
};

const toggleTheme = () => {
    isDark.value = !isDark.value;
    applyTheme();
};

onMounted(() => {
    const savedTheme = localStorage.getItem("theme");

    isDark.value = savedTheme === "dark";
    applyTheme();
});
</script>

<template>
    <button type="button"
        class="inline-flex size-10 items-center justify-center rounded-full bg-[#C8EB00] text-black transition duration-200 hover:opacity-90"
        :aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'" @click="toggleTheme">
        <svg v-if="isDark" xmlns="http://www.w3.org/2000/svg" class="size-4" viewBox="0 0 24 24" fill="none"
            stroke="currentColor" stroke-width="2">
            <circle cx="12" cy="12" r="4" />
            <path d="M12 2v2" />
            <path d="M12 20v2" />
            <path d="m4.93 4.93 1.41 1.41" />
            <path d="m17.66 17.66 1.41 1.41" />
            <path d="M2 12h2" />
            <path d="M20 12h2" />
            <path d="m6.34 17.66-1.41 1.41" />
            <path d="m19.07 4.93-1.41 1.41" />
        </svg>

        <svg v-else xmlns="http://www.w3.org/2000/svg" class="size-4" viewBox="0 0 24 24" fill="none"
            stroke="currentColor" stroke-width="2">
            <path d="M12 3a6 6 0 0 0 9 7.2A9 9 0 1 1 12 3Z" />
        </svg>
    </button>
</template>