<template>
    <section id="creation">
        <h1>Creation</h1>
        <div class="gallery">
            <div class="creation-section">
                <Production 
                    :image="PicShare2" 
                    :title="'PicShare'" 
                    :body="'ログイン機能、文章・画像・タグ投稿機能、タグ検索機能、投稿編集・削除機能を実装した簡易版Instagram。'" 
                    :body2="'読みやすいコードを意識しコーディングしました。また、デプロイまで自分で行った初めてのアプリです。'"
                    :url="'http://ryfiii.ddo.jp/'"
                    :github="'https://github.com/ryfiii/picshare'"
                    :skills="['PHP', 'Laravel', 'CSS', 'BootStrap', 'AWS', 'Linux']">
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
                    :image="WeatherApp" 
                    :title="'WeatherApp'"
                    :body="'OpenWeatherApiから天気を取得し、対応した背景に更新するアプリ'" 
                    :body2="''"
                    :url="'https://ryfiii-weatherapp.netlify.app/'"
                    :github="'https://github.com/ryfiii/WeatherApp'"
                    :skills="['JavaScript', 'HTML', 'CSS']">
                </Production>
                <Production 
                    :image="RestApi" 
                    :title="'RestApi'"
                    :body="'RestfulApiのサンプル。GET/POST/PUT/DELETEそれぞれのリクエストを送り、結果を取得できます。'" 
                    :body2="'ApiKeyの認証はLaravelのミドルウェアで行っています。'"
                    :url="''"
                    :github="'https://github.com/ryfiii/RestfulApi-sample'"
                    :skills="['PHP', 'Laravel', 'MySQL']">
                </Production>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Production from "@/components/Production.vue"

//写真インポート
import PicShare2 from "@/assets/images/creation/PicShare2.jpg"
import Sample_inc from "@/assets/images/creation/sample_inc.jpg"
import BlogSite from "@/assets/images/creation/RyuBlog.png"
import WeatherApp from "@/assets/images/creation/WeatherApp.jpg"
import RestApi from "@/assets/images/creation/restful-api.png"
</script>

<style scoped lang="scss">
#creation {
    padding: 50px 0;
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