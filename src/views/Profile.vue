<template>
    <section id="profile">
        <div class="about">
            <img src="https://picsum.photos/500/500" alt="">
            <div class="text">
                <h1>Ryunosuke</h1>
                <p>文系未経験から、Webエンジニアとして、様々な技術を勉強中です。</p>
                <p>PHP(Laravel)を主に勉強していますが、フロントエンドにも興味があります。</p> 
                <p>Githubにアプリの詳細な説明とソースコードを載せているので、ぜひ一度閲覧ください。</p>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
</script>

<style scoped lang="scss">
#profile {
    height: 500px;
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