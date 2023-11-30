<template>
  <div class="skill-block" @mouseover="showModal = true" @mouseleave="showModal = false">
    <div class="text">
      <img :src="props.icon" />
      <h2>{{ props.name }}</h2>
    </div>
    <Gauge v-if="props.level" :value="props.level" />
    <SkillModal v-if="showModal && text" :text="props.text"></SkillModal>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue'
import Gauge from '@/components/Gauge.vue'
import SkillModal from './SkillModal.vue'

interface Props {
  icon: string
  name: string
  text?: string
  level?: number
}

const props = defineProps<Props>();

const showModal = ref(false)
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

.skill-block {
  @include flexCenter;
  flex-direction: column;
  background-color: white;
  border-radius: 10px;
  margin-right: 30px;
  margin-top: 30px;
  padding: 10px 35px;
  box-shadow: 0px 10px 18px -3px #777777;
  transition: transform 0.4s;
  position: relative;

  &:hover {
    transform: scale(1.1);
  }

  .text {
    @include flexCenter;
    margin-bottom: 5px;

    img {
      width: 30px;
      height: 30px;
      margin-right: 8px;
    }
  }
}
</style>