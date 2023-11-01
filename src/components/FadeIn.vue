<template>
    <div ref="fade" :class="{ 'animate__animated animate__fadeIn': visible }">
      <slot></slot>
    </div>
  </template>
  
  <script setup lang="ts">
  import { ref, onMounted, onBeforeUnmount } from 'vue';
  
  const fade = ref<HTMLElement | null>(null);
  const visible = ref<boolean>(false);
  
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
  </script>
  