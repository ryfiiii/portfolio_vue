<template>
    <section id="skill">
        <SlideInLeft>
            <div class="frontend">
                <h1>フロントエンド</h1>
                <div class="skill-section">
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" />
                            <h2>HTML</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" />
                            <h2>CSS</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img
                                src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" />
                            <h2>JavaScript</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" />
                            <h2>Vue.js</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img
                                src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" />
                            <h2>BootStrap</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sass/sass-original.svg" />
                            <h2>Sass</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                </div>
            </div>
        </SlideInLeft>

        <SlideInRight>
            <div class="backend">
                <h1>バックエンド</h1>
                <div class="skill-section">
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" />
                            <h2>PHP</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain.svg" />
                            <h2>Laravel</h2>
                        </div>
                        <Gauge :value="4"></Gauge>
                    </div>
                    <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" />
                            <h2>MySQL</h2>
                        </div>
                        <Gauge :value="3"></Gauge>
                    </div>
                    <!-- <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" />
                            <h2>PostgreSQL</h2>
                        </div>
                        <Gauge :value="3"></Gauge>
                    </div> -->
                    <!-- <div class="skill-block">
                        <div class="text">
                            <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" />
                            <h2>Java</h2>
                        </div>
                        <Gauge :value="3"></Gauge>
                    </div> -->
                </div>
            </div>
        </SlideInRight>

        <SlideInLeft>
            <div class="tool-others">
                <h1>ツール / その他</h1>
                <div class="oowaku">
                    <div class="skill-section">
                        <div class="skill-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg">
                                <h2>VSCode</h2>
                            </div>
                            <Gauge :value="5"></Gauge>
                        </div>
                        <div class="skill-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" />
                                <h2>Git</h2>
                            </div>
                            <Gauge :value="4"></Gauge>
                        </div>
                        <div class="skill-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" />
                                <h2>Github</h2>
                            </div>
                            <Gauge :value="4"></Gauge>
                        </div>
                        <div class="skill-block">
                            <div class="text">
                                <img
                                    src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg" />
                                <h2>Windows</h2>
                            </div>
                            <Gauge :value="5"></Gauge>
                        </div>
                    </div>
                </div>
            </div>
        </SlideInLeft>

        <SlideInRight>
            <div class="interest">
                <h1>勉強中</h1>
                <div class="oowaku">
                    <div class="skill-section">
                        <div class="interest-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg">
                                <h2>TailwindCss</h2>
                            </div>
                        </div>
                        <div class="interest-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" />
                                <h2>Java</h2>
                            </div>
                        </div>
                        <div class="interest-block">
                            <div class="text">
                                <img
                                    src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" />
                                <h2>Spring</h2>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </SlideInRight>

        <SlideInLeft>
            <div class="interest">
                <h1>興味がある</h1>
                <div class="oowaku">
                    <div class="skill-section">
                        <div class="interest-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg">
                                <h2>React</h2>
                            </div>
                        </div>
                        <div class="interest-block">
                            <div class="text">
                                <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg" />
                                <h2>Nuxt.js</h2>
                            </div>
                        </div>
                        <div class="interest-block">
                            <div class="text">
                                <img
                                    src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/wordpress/wordpress-original.svg" />
                                <h2>WordPress</h2>
                            </div>
                        </div>
                        <div class="interest-block">
                        <div class="text">
                            <img
                                src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" />
                            <h2>TypeScript</h2>
                        </div>
                    </div>
                    </div>
                </div>
            </div>
        </SlideInLeft>
    </section>
</template>

<script setup lang="ts">
import Gauge from "@/components/Gauge.vue"
import SlideInLeft from "@/components/SlideInLeft.vue"
import SlideInRight from "@/components/SlideInRight.vue"
</script>

<style scoped lang="scss">
@import "../assets/css/validate-function";

#skill {
    width: 100%;
    height: 100%;
    padding-top: 5px;
    padding-bottom: 70px;
    @include flexCenter;
    flex-direction: column;
    background: url("../assets/images/dog-megane.jpg");
    background-size: cover;
    background-position: center;
    background-attachment: fixed;
    @include mq(){
        background: url("");
        background-color: #dddddd;
        background-attachment: scroll;
    }

    .frontend,
    .backend,
    .tool-others,
    .interest {
        margin-top: 90px;
        @include flexCenter;
        flex-direction: column;

        h1 {
            text-align: center;
            color: white;
            margin: 50px 0 10px 0;
            @include mq(){
                margin: 0;
                color: #2c3e50;
            }
        }

        .skill-section {
            max-width: 1400px;
            @include flexCenter;
            flex-wrap: wrap;
            margin: 0 0 30px 0;

            .skill-block {
                @include flexCenter;
                flex-direction: column;
                background-color: white;
                border-radius: 10px;
                margin-right: 30px;
                margin-top: 30px;
                padding: 10px 35px;
                box-shadow: 0px 10px 18px -3px #777777;
                transition: transform 0.4s;

                &:hover {
                    transform: scale(1.1);
                }

                .text {
                    @include flexCenter;
                    margin-bottom: 5px;

                    img {
                        width: 30px;
                        height: 30px;
                        margin-right: 8px;
                    }
                }
            }

            .interest-block {
                @include flexCenter;
                flex-direction: column;
                background-color: white;
                border-radius: 10px;
                margin-right: 30px;
                margin-top: 30px;
                padding-top: 4px;
                width: 236px;
                height: 65px;
                box-shadow: 0px 10px 18px -3px #777777;
                transition: transform 0.4s;

                &:hover {
                    transform: scale(1.1);
                }

                .text {
                    @include flexCenter;
                    margin-bottom: 5px;

                    img {
                        width: 30px;
                        height: 30px;
                        margin-right: 8px;
                    }
                }
            }
        }
    }
}
</style>