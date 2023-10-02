<template>
    <section id="splash">
        <h1 class="animated__animate animate__bounceIn animate__slow">Ryunosuke's PortFolio</h1>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

#splash {
    width: 100%;
    height: 100vh;
    background: url("../assets/images/sea.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    @include flexCenter;
    @include mq(){
        background-attachment: scroll;
    }

    h1 {
        font-size: 3.5rem;
        color: white;
        text-shadow: rgba(0, 0, 0, 0.2) 0px 0px 10px;
        @include mq(){
            font-size: 2.2rem;
            text-align: center;
            padding: 0 20px;
        }
    }
}
</style>