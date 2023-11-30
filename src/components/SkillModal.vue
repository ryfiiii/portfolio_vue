<template>
  <div class="skill-modal">
    <p>{{ props.text }}</p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  text: String,
})
</script>

<style scoped lang="scss">
.skill-modal {
  position: absolute;
  width: 100%;
  padding: 10px;
  background-color: rgb(255, 255, 255);
  top: -220%;
  left: 50%;
  transform: translateX(-50%);
  box-shadow: 0px 10px 18px -3px #777777;
  border-radius: 10px;

  p {
    font-size: 0.8rem;
  }
}
</style>
