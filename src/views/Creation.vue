<template>
    <section id="creation">
        <h1>Creation</h1>
        <div class="gallery">
            <div class="creation-section">
                <Production 
                    :image="PortFolio" 
                    :title="'PortFolio'" 
                    :body="'私が使用できる、技術・技術レベル・制作物 等を紹介するために作成しました。'" 
                    :body2="'制作物のソースコードはGithubのアイコンをクリックすることで見ることができます。'"
                    :url="'https://ryfiii-portfolio.netlify.app/'"
                    :github="'https://github.com/ryfiii/portfolio_vue'"
                    :skills="['Vue.js', 'TypeScript', 'Sass']">
                </Production>
                <Production 
                    :image="PicShare" 
                    :title="'PicShare'" 
                    :body="'ログイン機能、文章・画像・タグ投稿機能、タグ検索機能、投稿編集・削除機能を実装した簡易版Instagram。読みやすいコードを意識しながらコーディングし、デプロイまで行いました。'" 
                    :body2="'sample@sample.com / sample123 でログインできます'"
                    :url="'http://ryfiii.ddo.jp/'"
                    :github="'https://github.com/ryfiii/picshare'"
                    :skills="['PHP', 'Laravel', 'CSS', 'BootStrap', 'AWS', 'Linux', 'LightSail']">
                </Production>
                <Production 
                    :image="Sample_inc" 
                    :title="'サンプル株式会社ウェブサイト'" 
                    :body="'Vue.js3の練習用に作成しました。'" 
                    :body2="'ロードアニメーションや切り替えアニメーションを実装しています。'"
                    :url="'https://vue-sampleinc-website.netlify.app/'"
                    :github="'https://github.com/ryfiii/vue_samplesite'"
                    :skills="['Vue.js', 'Sass']">
                </Production>
                <Production 
                    :image="BlogSite" 
                    :title="'ブログサイト'" 
                    :body="'Vue.jsとMicroCMSを組み合わせて、ブログサイトを作成しました。'" 
                    :body2="'Axiosを使用して、MicroCMSで作成したブログを取得しています。'"
                    :url="'https://ryfiii-blog.netlify.app/'"
                    :github="'https://github.com/ryfiii/blog'"
                    :skills="['Vue.js', 'Sass', 'MicroCMS']">
                </Production>
                <Production 
                    :image="RealtimeChat" 
                    :title="'RealtimeChat'"
                    :body="'LINEのようにリアルタイムでやり取りができるチャットアプリ'"
                    :body2="'PusherとLaravel Echoを活用して、ユーザー間のリアルタイムな対話を可能にし、且つデータベースに情報を保存し永続化を実現しています。'"
                    :url="'https://ryfiii-404-notfound.vercel.app/'"
                    :github="'https://github.com/ryfiii/ChatApp_VuexLaravel'"
                    :skills="['Vue.js', 'Laravel', 'Pusher', 'Laravel Echo', 'Sass', 'MySQL', 'Laravel UI']">
                </Production>
                <Production 
                    :image="WeatherApp" 
                    :title="'WeatherApp'"
                    :body="'OpenWeatherApiから天気を取得し、対応した背景に更新するアプリ'" 
                    :body2="'　'"
                    :url="'https://ryfiii-weatherapp.netlify.app/'"
                    :github="'https://github.com/ryfiii/WeatherApp'"
                    :skills="['JavaScript', 'HTML', 'CSS']">
                </Production>
                <Production 
                    :image="RestApi" 
                    :title="'RestApi'"
                    :body="'RestfulApiのサンプル。GET/POST/PUT/DELETEそれぞれのリクエストを送り、結果を取得できます。'" 
                    :body2="'ApiKeyの認証はLaravelのミドルウェアで行っています。'"
                    :url="'https://ryfiii-404-notfound.vercel.app/'"
                    :github="'https://github.com/ryfiii/RestfulApi-sample'"
                    :skills="['PHP', 'Laravel', 'MySQL']">
                </Production>
                <Production 
                    :image="VueLaravelTodo" 
                    :title="'Vue × Laravel TodoApp'"
                    :body="'Laravelを用いてDBとの通信を行うAPIを作成しました。'" 
                    :body2="'フロントにVue.jsを使用し、axiosでAPIを呼び出してデータを取得し、表示内容を動的に更新しています。'"
                    :url="'https://ryfiii-404-notfound.vercel.app/'"
                    :github="'https://github.com/ryfiii/Todo_Laravel'"
                    :skills="['PHP', 'Laravel', 'MySQL', 'Vue.js', 'BootStrap']">
                </Production>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Production from "@/components/Production.vue"

//写真インポート
import PortFolio from "@/assets/images/creation/vue-portfolio.png"
import PicShare from "@/assets/images/creation/PicShare.png"
import Sample_inc from "@/assets/images/creation/SampleInc.png"
import BlogSite from "@/assets/images/creation/RyuBlog.png"
import WeatherApp from "@/assets/images/creation/WeatherApp.png"
import RestApi from "@/assets/images/creation/RestfulApi.png"
import VueLaravelTodo from "@/assets/images/creation/Vue_Laravel_TodoApp.png"
import RealtimeChat from "@/assets/images/creation/RealtimeChat.png"
</script>

<style scoped lang="scss">
#creation {
    padding: 50px 0 100px 0;
    background-color: white;

    h1 {
        text-align: center;
        font-size: 1.8rem;
    }

    .gallery {
        .creation-section {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }
    }
}
</style>