<template>
    <section id="profile">
        <div class="about">
            <img src="https://picsum.photos/500/500" alt="">
            <div class="text">
                <h1>Ryunosuke</h1>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Blanditiis, maxime sit quas repellendus
                    voluptas repudiandae est, placeat consequuntur vitae dicta et iusto fugit! Sint illum quia ut
                    repudiandae, tenetur recusandae.</p>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
#profile {
    height: 100vh;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;

    &::after {
        content: "Profile";
        color: rgb(81, 173, 254);
        font-size: 2.0rem;
        display: flex;
        align-items: center;
        justify-content: center;
        position: absolute;
        width: 200px;
        height: 50px;
        top: -50px;
        left: 50%;
        transform: translateX(-50%);
        background-color: white;
        z-index: 5;
        border-top-right-radius: 8px;
        border-top-left-radius: 8px;
    }

    .about {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 80%;

        img {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 50%;
        }

        .text {
            margin-left: 20px;

            h1 {
                font-size: 1.5rem;
                margin-bottom: 10px;
            }

            p {
                font-size: 1.1rem;
            }
        }
    }
}</style>