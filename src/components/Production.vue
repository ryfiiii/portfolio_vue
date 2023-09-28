<template>
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
</template>

<script setup lang="ts">
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
.production {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 1100px;
    height: 270px;
    border-radius: 10px;
    box-shadow: 0px 10px 18px -3px #777777;
    margin-top: 40px;

    img {
        display: block;
        width: 400px;
        height: 270px;
        object-fit: cover;
    }

    .text {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        h2 {
            font-size: 1.7rem;
            text-align: center;
            margin: 25px 0;

            i {
                margin-left: 10px;
            }
        }

        p {
            font-size: 1.1rem;
            padding: 0 25px;
        }

        .skill {
            display: flex;
            margin-top: 20px;
            span {
                display: block;
                background-color: #ccc;
                margin-right: 10px;
                padding: 5px 10px;
                border-radius: 20px;
            }
        }
    }
}
</style>