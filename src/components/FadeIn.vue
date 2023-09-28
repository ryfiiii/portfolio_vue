<template>
    <div ref="fade" :class="{ fadein: visible, hidden: !visible }">
        <slot></slot>
    </div>
</template>
  
<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const visible = ref<Boolean>(false)
const fade = ref<HTMLElement | null>(null)

const handleScroll = () => {
    if (!visible.value && fade.value) {
        const top = fade.value.getBoundingClientRect().top
        visible.value = (top + 100) < window.innerHeight
    }
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>
  
<style scoped>
.hidden {
    opacity: 0;
}

.fadein {
    animation: fadeIn 1s;
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
  