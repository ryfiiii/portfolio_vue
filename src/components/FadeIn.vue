<template>
    <div ref="fade" :class="{ fadein: visible, hidden: !visible }">
        <slot></slot>
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue';

const fade = ref<HTMLElement | null>(null);
const visible = ref(false);

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.target === fade.value) {
            visible.value = entry.isIntersecting;
        }
    });
}, {
    threshold: 0.1
});

onMounted(() => {
    if (fade.value) {
        observer.observe(fade.value);
    }
});

onBeforeUnmount(() => {
    if (fade.value) {
        observer.unobserve(fade.value);
    }
});
</script>

<style scoped>
.hidden {
    opacity: 0;
}

.fadein {
    animation: fadeIn 1.0s;
    opacity: 1;
}

@keyframes fadeIn {
    0% {
        opacity: 0;
        transform: translateY(50px);
    }

    100% {
        opacity: 1;
        transform: translateX(0px);
    }
}
</style>
