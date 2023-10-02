<template>
    <FadeIn>
        <div class="production">
            <a :href="url" target="_blank" rel="noopener noreferrer">
                <img :src="image">
            </a>
            <div class="text">
                <h2>
                    <a :href="url" target="_blank" rel="noopener noreferrer">{{ title }}</a>
                    <span>
                        <a :href="github" target="_blank" rel="noopener noreferrer"><i class="fa-brands fa-github"></i></a>
                    </span>
                </h2>
                <p>{{ body }}</p>
                <p>{{ body2 }}</p>
                <div class="skill">
                    <span v-for="skill in skills" :key="skill">{{ skill }}</span>
                </div>
            </div>
        </div>
    </FadeIn>
</template>

<script setup lang="ts">
import FadeIn from "@/components/FadeIn.vue"

const props = defineProps<{
    image: string,
    title: string,
    body: string,
    body2: string,
    url: string,
    github: string,
    skills: string[],
}>()
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";
.production {
    display: flex;
    width: 1100px;
    height: 270px;
    border-radius: 10px;
    box-shadow: 0px 10px 18px -3px #777777;
    margin-top: 40px;
    @include mq(){
        width: 300px;
        height: auto;
        flex-direction: column;
        padding-bottom: 20px;
    }

    img {
        display: block;
        width: 400px;
        height: 270px;
        object-fit: cover;
        border-top-left-radius: 10px;
        border-bottom-left-radius: 10px;
        border-right: 1px solid #ccc;
        @include mq(){
            width: 300px;
            border-top-right-radius: 10px;
            border-bottom-left-radius: 0;
        }
    }

    .text {
        display: flex;
        justify-content: center;
        flex-direction: column;
        margin-left: 30px;

        h2 {
            font-size: 1.7rem;
            text-align: center;
            margin: 25px 0;

            i {
                text-align: center;
                margin-left: 10px;
            }
        }

        p {
            font-size: 1.1rem;
            padding: 0 25px;
        }

        .skill {
            display: flex;
            justify-content: center;
            margin-top: 20px;
            flex-wrap: wrap;

            span {
                display: block;
                background-color: #ccc;
                margin-right: 10px;
                padding: 5px 10px;
                border-radius: 20px;
                margin-bottom: 10px;
            }
        }
    }

    transition: transform 0.4s;

    &:hover {
        transform: scale(1.05);
    }
}
</style>