<template>
    <div>
        <header :class="{ 'light': isScreenTop }">
            <nav>
                <div class="logo">
                    <h1 v-if="isScreenTop">PortFolio</h1>
                </div>
                <ul>
                    <li><a href="#profile" v-smooth-scroll>Profile</a></li>
                    <li><a href="#skill" v-smooth-scroll>Skill</a></li>
                    <li><a href="#creation" v-smooth-scroll>Creation</a></li>
                    <li><a href="#contact" v-smooth-scroll>Contact</a></li>
                </ul>
            </nav>
        </header>
        <div class="pageTop" v-if="isScreenTop">
            <a href="#splash" v-smooth-scroll><i class="fa-solid fa-angles-up"></i></a>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount, watchEffect } from 'vue';

const scrollY = ref(0);
const isScreenTop = ref(false);

const onScroll = () => {
    scrollY.value = window.pageYOffset;
};

watchEffect(() => {
    isScreenTop.value = scrollY.value > 0;
});

onMounted(() => {
    window.addEventListener('scroll', onScroll);
});

onBeforeUnmount(() => {
    window.removeEventListener('scroll', onScroll);
});
</script>

<style scoped lang="scss">
header {
    width: 100%;
    position: absolute;
    transition: all 0.5s;

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 50px;

        .logo {
            margin-left: 30px;
        }

        ul {
            display: flex;
            justify-content: center;
            align-items: center;

            li {
                list-style: none;

                &:last-child {
                    margin-right: 60px;
                }

                a {
                    text-decoration: none;
                    padding: 12px 15px;

                    &:hover {
                        background-color: #ffffff6e;
                    }
                }
            }
        }
    }

    &.light {
        background-color: rgb(243, 243, 243);
        position: fixed;
        z-index: 10;
    }
}

.pageTop {
    position: fixed;
    bottom: 4%;
    right: 2%;
    background-color: rgb(217, 217, 217);
    border: 3px solid rgb(169, 169, 169);
    border-radius: 5px;
    width: 50px;
    height: 50px;
    color: rgb(152, 152, 152);
    font-size: 38px;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    z-index: 100;

    i {
        color: rgb(152, 152, 152);
    }
}
</style>
