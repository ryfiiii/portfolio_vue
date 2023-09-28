<template>
    <section id="skill">
        <div class="frontend">
            <h1>フロントエンド</h1>
            <div class="skill-section">
                <div class="skill-block">
                    <div class="text">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" />
                        <h2>HTML</h2>
                    </div>
                    <Gauge :value="5"></Gauge>
                </div>
                <div class="skill-block">
                    <div class="text">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" />
                        <h2>CSS</h2>
                    </div>
                    <Gauge :value="5"></Gauge>
                </div>
                <div class="skill-block">
                    <div class="text">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" />
                        <h2>JavaScript</h2>
                    </div>
                    <Gauge :value="4"></Gauge>
                </div>
                <div class="skill-block">
                    <div class="text">            
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" />
                        <h2>TypeScript</h2>
                    </div>
                    <Gauge :value="3"></Gauge>
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
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" />
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
                    <Gauge :value="5"></Gauge>
                </div>
                <div class="skill-block">
                    <div class="text">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" />
                        <h2>MySQL</h2>
                    </div>
                    <Gauge :value="4"></Gauge>
                </div>
                <div class="skill-block">
                    <div class="text">
                        <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" />
                        <h2>Java</h2>
                    </div>
                    <Gauge :value="3"></Gauge>
                </div>
            </div>
        </div>

        <div class="tool-others">
            <h1>ツール / その他</h1>
            <div class="oowaku">
                <div class="skill-section">
                <div class="skill-block">
                    <div class="text">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg">
                        <h2>VSCode</h2>
                    </div>
                    <Gauge :value="4"></Gauge>
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
            </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Gauge from "@/components/Gauge.vue"
</script>

<style scoped lang="scss">
#skill {
    padding: 50px 0;
    background: url("../assets/images/dog-megane.jpg");
    background-position: center;
    background-size: cover;
    background-attachment: fixed;

    .frontend, .backend, .tool-others {

        h1 {
            text-align: center;
            color: white;
        }
        
        .skill-section {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-wrap: wrap;
            margin: 0 auto 30px auto;

            .skill-block {
                display: flex;
                justify-content: center;
                align-items: center;
                flex-direction: column;
                background-color: white;
                border-radius: 10px;
                margin-right: 30px;
                margin-top: 20px;
                padding: 10px 35px;
                box-shadow: 0px 10px 18px -3px #777777;

                .text {
                    display: flex;
                    justify-content: center;
                    align-items: center;
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
}</style>