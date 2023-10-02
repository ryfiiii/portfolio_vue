<template>
    <section id="profile">
        <h1>Profile</h1>
        <div class="about">
            <img src="../assets/images/apple.jpg" alt="">
            <FadeIn>
                <div class="text">
                    <h1>Ryunosuke</h1>
                    <p>文系未経験から、Webエンジニアとして、様々な技術を勉強中です。</p>
                    <p>PHP(Laravel)を主に勉強していますが、フロントエンドにも興味があります。</p>
                    <p>Githubにアプリの詳細な説明とソースコードを載せているので、ぜひ一度閲覧ください。</p>
                </div>
            </FadeIn>
        </div>
    </section>
</template>

<script setup lang="ts">
import FadeIn from "@/components/FadeIn.vue"
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

#profile {
    background-color: #fff;
    padding: 130px 0 200px 0;
    @include flexCenter;
    flex-direction: column;
    @include mq(){
        padding: 50px 0;
    }

    h1 {
        font-size: 2.5rem;
        margin-bottom: 70px;
        @include mq(){
            margin-bottom: 0;
        }
    }

    .about {
        width: 80%;
        @include flexCenter;
        @include mq(){
            flex-direction: column;
        }

        img {
            width: 200px;
            height: 200px;
            object-fit: cover;
            border-radius: 50%;
            @include mq(){
                margin: 60px 0;
            }
        }

        .text {
            margin-left: 20px;
            @include mq(){
                text-align: center;
            }

            h1 {
                font-size: 1.5rem;
                margin-bottom: 10px;
                @include mq(){
                    font-size: 1.7rem;
                    margin-bottom: 30px;
                }
            }

            p {
                font-size: 1.1rem;
            }
        }
    }
}
</style>