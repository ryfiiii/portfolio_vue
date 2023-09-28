<template>
    <div class="rating">
        <div v-for="index in 5" :key="index" :style="getGaugeColor(index)" class="gauge"></div>
    </div>
</template>
  
<script setup lang="ts">

const props = defineProps<{
    value: number
}>()

const getGaugeColor = (index: number) => {
    return {
        backgroundColor: index <= props.value ? 'gold' : 'lightgray',
    }
}
</script>
  
<style scoped lang="scss">
.rating {
    display: flex;
}

.gauge {
    width: 30px;
    height: 10px;
    margin-right: 4px;

    &:last-child {
        margin-right: 0;
    }
}
</style>
  