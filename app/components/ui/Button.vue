<script setup>
const props = defineProps({
    to: {
        type: String,
        default: "",
    },
    href: {
        type: String,
        default: "",
    },
    type: {
        type: String,
        default: "button",
    },
    variant: {
        type: String,
        default: "primary",
    },
    size: {
        type: String,
        default: "md",
    },
    isLoading: {
        type: Boolean,
        default: false,
    },
    disabled: {
        type: Boolean,
        default: false,
    },
});

const variantClass = computed(() => {
    const classes = {
        primary: "btn-primary",
        hero: "btn-hero",
    };

    return classes[props.variant] || classes.primary;
});

const sizeClass = computed(() => {
    const classes = {
        sm: "btn-sm",
        md: "btn-md",
        lg: "btn-lg",
    };

    return classes[props.size] || classes.md;
});

const buttonClass = computed(() => [
    "btn-base",
    variantClass.value,
    sizeClass.value,
]);

const isDisabled = computed(() => props.disabled || props.isLoading);
</script>

<template>
    <NuxtLink v-if="to" :to="to" :class="buttonClass">
        <span v-if="isLoading" class="btn-loader"></span>
        <slot />
    </NuxtLink>

    <a v-else-if="href" :href="href" :class="buttonClass" target="_blank" rel="noopener noreferrer">
        <span v-if="isLoading" class="btn-loader"></span>
        <slot />
    </a>

    <button v-else :type="type" :disabled="isDisabled" :class="buttonClass">
        <span v-if="isLoading" class="btn-loader"></span>
        <slot />
    </button>
</template>