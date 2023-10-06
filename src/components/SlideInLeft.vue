<template>
  <div ref="slide" :class="{ 'animate__animated animate__fadeInLeft': visible }">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from 'vue';

const slide = ref<HTMLElement | null>(null);
const visible = ref(false);

const handleScroll = () => {
  if (slide.value && !visible.value) {
    const top = slide.value.getBoundingClientRect().top;
    visible.value = (top + 100) < window.innerHeight;
  }
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>
