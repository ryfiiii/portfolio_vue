<template>
    <div ref="fade" :class="{ slidein: visible, hidden: !visible }">
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

.slidein {
  animation: slideIn 1s;
  opacity: 1;
}

@keyframes slideIn {
  0% {
    -webkit-transform: translate3d(-200vh, 0, 0);
    transform: translate3d(-200vh, 0, 0);
  }
  100% {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}
</style>