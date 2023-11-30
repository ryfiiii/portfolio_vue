<template>
  <div class="interest-block">
    <div class="text">
      <img :src="props.icon" />
      <h2>{{ props.name }}</h2>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

interface Props {
  icon: string;
  name: string;
}

const props = defineProps<Props>();
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

.interest-block {
  @include flexCenter;
  flex-direction: column;
  background-color: white;
  border-radius: 10px;
  margin-right: 30px;
  margin-top: 30px;
  padding-top: 4px;
  width: 236px;
  height: 65px;
  box-shadow: 0px 10px 18px -3px #777777;
  transition: transform 0.4s;

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