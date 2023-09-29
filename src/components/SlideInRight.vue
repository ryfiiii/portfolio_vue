<template>
  <div class="overflow">
    <div ref="fade" :class="{ slidein: visible, hidden: !visible }">
      <slot></slot>
    </div>
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
.overflow {
  overflow: hidden;
}

.hidden {
  opacity: 0;
}

.slidein {
  animation: slideIn 0.8s;
  opacity: 1;
}

@keyframes slideIn {
  0% {
    -webkit-transform: translate3d(200vh, 0, 0);
    transform: translate3d(200vh, 0, 0);
  }

  100% {
    -webkit-transform: translate3d(0, 0, 0);
    transform: translate3d(0, 0, 0);
  }
}
</style>
