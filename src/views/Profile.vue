<template>
    <section id="profile">
        <h1 class="title">~はじめに~</h1>
        <div class="about">
            <img src="../assets/images/apple.jpg" alt="">
            <FadeIn>
                <div class="text">
                    <h1>Ryunosuke</h1>
                    <p>2023年4月に新卒としてIT業界に足を踏み入れました。</p>
                    <br>
                    <p>研修では、2か月間Javaのスクールで基礎を学び、その後は独学でJavaScriptやPHPを中心に様々なプログラミング言語やフレームワークに触れ、実践的なプロジェクトを通じてスキルアップを図ってきました。</p>
                    <br>
                    <p>ウェブ開発についての知識を深めていく中で、要件定義を行えるフルスタックエンジニアを志すようになりました。現代のウェブ開発技術に対して熱心に学び、未来のプロジェクトに貢献できるよう、常にスキルの向上を求め、全力を尽くしています。</p>
                    <br>
                    <p>現在所属している会社では、Javaの古い技術を使用した保守作業や、ローコード開発案件、未経験のC#の組み込みに関する案件が主に提案されています。これらも学びの場ではありますが、私の目標により密接に関わるチャンスを求めて、新たな環境を探しています。</p>
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
    width: 80%;
    margin: 0 auto;
    @include mq(){
        padding: 50px 0;
    }

    .title {
        text-align: center;
        text-shadow: 2px 3px 3px rgba(0, 0, 0, 0.4);
    }

    h1 {
        font-size: 2.5rem;
        margin-bottom: 70px;
        @include mq(){
            margin-bottom: 0;
        }
    }

    .about {
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