<template>
    <section id="splash">
        <h1>Ryunosuke's PortFolio</h1>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
#splash {
    width: 100%;
    height: 100vh;
    background: url("../assets/images/sea.jpg");
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
    display: flex;
    justify-content: center;
    align-items: center;

    h1 {
        font-size: 3.5rem;
        color: white;
        text-shadow: rgba(0, 0, 0, 0.2) 0px 0px 10px;
    }
}
</style>