<template>
    <div ref="fade" :class="{ fadein: visible, hidden: !visible }">
        <slot></slot>
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount, watchEffect } from 'vue';

const fade = ref<HTMLElement | null>(null);
const visible = ref(false);

const handleScroll = () => {
    if (fade.value && !visible.value) {
        const top = fade.value.getBoundingClientRect().top;
        visible.value = (top + 100) < window.innerHeight;
    }
};

onMounted(() => {
    window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
    window.removeEventListener('scroll', handleScroll);
});

watchEffect(() => {
    handleScroll();
});
</script>

<style scoped>
.hidden {
    opacity: 0;
}

.fadein {
    animation: fadeIn 1.5s;
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