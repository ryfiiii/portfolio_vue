<template>
  <section id="creation">
    <h1>Creation</h1>
    <p class="details">
      これまでに学んできた知識を定着させるために制作した作品をいくつか紹介しています。使用した技術スタックやソースコードも公開しておりますので、詳細についてご覧いただけます。お時間が許す際に、ぜひご確認ください。
    </p>
    <div class="gallery">
      <div class="creation-section">
        <Production :image="PortFolio" :title="'PortFolio'" :body="'私が使用できる、技術・技術レベル・制作物 等を紹介するために作成しました。'"
          :body2="'制作物のソースコードはGithubのアイコンをクリックすることで見ることができます。'" :url="'https://ryfiii-portfolio.vercel.app/'"
          :github="null" :skills="['Vue.js', 'TypeScript', 'Sass']">
        </Production>
        <Production :image="PicShare" :title="'PicShare'"
          :body="'ログイン機能、文章・画像・タグ投稿機能、タグ検索機能、投稿編集・削除機能を実装した簡易版Instagram。読みやすいコードを意識しながらコーディングし、デプロイまで行いました。'" :body2="''"
          :url="'https://github.com/ryfiiii/PicShare'" :github="'https://github.com/ryfiiii/PicShare'"
          :skills="['Laravel', 'BootStrap', 'AWS', 'Linux']">
        </Production>
        <Production :image="ExpressVueChatapp" :title="'RealTimeChat(express)'" :body="'FrontendとBackendが完全に独立したチャットアプリ'"
          :body2="'ファイルを含むデータの受け渡しはjson形式で行っており、チャットイベントの検知はsocket.ioを使用しています。'"
          :url="'https://github.com/ryfiiii/vue_express_chatapp'"
          :github="'https://github.com/ryfiiii/vue_express_chatapp'"
          :skills="['Express', 'Vue.js', 'TypeScript', 'socket.io', 'MySQL', 'Prisma']">
        </Production>
        <Production :image="Sample_inc" :title="'サンプル株式会社ウェブサイト'" :body="'Vue.js3の練習用に作成しました。'"
          :body2="'ロードアニメーションや切り替えアニメーションを実装しています。'" :url="'https://vue-sampleinc-website.netlify.app/'"
          :github="'https://github.com/ryfiiii/vue_samplesite'" :skills="['Vue.js', 'Sass']">
        </Production>
        <Production :image="Laravel_Stripe_Shop" :title="'StripeShop'" :body="'購入したブログのみを閲覧できる、ブログショッピングアプリです。'"
          :body2="'決済システムにはStripe、ブログにはMicroCMSを使用しています。'" :url="'https://github.com/ryfiiii/Laravel_Stripe_Blog/'"
          :github="'https://github.com/ryfiiii/Laravel_Stripe_Blog'"
          :skills="['Laravel', 'Stripe', 'MicroCMS', 'TailwindCss', 'MySQL']">
        </Production>
        <Production :image="BlogSite" :title="'ブログサイト'" :body="'Vue.jsとMicroCMSを組み合わせて、ブログサイトを作成しました。'"
          :body2="'Axiosを使用して、MicroCMSで作成したブログを取得しています。'" :url="'https://ryfiii-blog.netlify.app/'"
          :github="'https://github.com/ryfiiii/blog'" :skills="['Vue.js', 'Sass', 'MicroCMS']">
        </Production>
        <Production :image="RealtimeChat" :title="'RealtimeChat(Laravel)'" :body="'LINEのようにリアルタイムでやり取りができるチャットアプリ'"
          :body2="'PusherとLaravel Echoを活用して、ユーザー間のリアルタイムな対話を可能にし、且つデータベースに情報を保存し永続化を実現しています。'"
          :url="'https://github.com/ryfiiii/ChatApp_VuexLaravel'"
          :github="'https://github.com/ryfiiii/ChatApp_VuexLaravel'"
          :skills="['Vue.js', 'Laravel', 'Pusher', 'Laravel Echo', 'Sass', 'MySQL']">
        </Production>
        <Production :image="ExpressTsRestapi" :title="'express-ts-restapi'"
          :body="'Express, Typescript, Prismaを使用して作成した簡単なRestfulApi'" :body2="'GET/POST/PUT/DELETE それぞれのリクエストに対応しています。'"
          :url="'https://github.com/ryfiiii/express_ts_restapi/'"
          :github="'https://github.com/ryfiiii/express_ts_restapi'"
          :skills="['Node.js', 'Express', 'TypeScript', 'Prisma']">
        </Production>
        <Production :image="WeatherApp" :title="'WeatherApp'" :body="'OpenWeatherApiから天気を取得し、対応した背景に更新するアプリ'" :body2="'　'"
          :url="'https://ryfiii-weatherapp.netlify.app/'" :github="'https://github.com/ryfiiii/weatherapp'"
          :skills="['JavaScript', 'HTML', 'CSS']">
        </Production>
        <!-- <Production :image="RestApi" :title="'RestApi'"
          :body="'RestfulApiのサンプル。GET/POST/PUT/DELETEそれぞれのリクエストを送り、結果を取得できます。'"
          :body2="'ApiKeyの認証はLaravelのミドルウェアで行っています。'" :url="'https://github.com/ryfiiii/RestfulApi-sample'"
          :github="'https://github.com/ryfiiii/RestfulApi-sample'" :skills="['PHP', 'Laravel', 'MySQL']">
        </Production> -->
        <!-- <Production :image="VueLaravelTodo" :title="'Vue × Laravel TodoApp'" :body="'Laravelを用いてDBとの通信を行うAPIを作成しました。'"
          :body2="'フロントにVue.jsを使用し、axiosでAPIを呼び出してデータを取得し、表示内容を動的に更新しています。'"
          :url="'https://github.com/ryfiiii/Todo_Laravel/'" :github="'https://github.com/ryfiiii/Todo_Laravel'"
          :skills="['PHP', 'Laravel', 'MySQL', 'Vue.js', 'BootStrap']">
        </Production> -->
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
import Laravel_Stripe_Shop from "@/assets/images/creation/laravel_stripe_shop.png"
import ExpressTsRestapi from "@/assets/images/creation/express-ts-restapi.png"
import ExpressVueChatapp from "@/assets/images/creation/express_vue_chatapp.png"
</script>

<style scoped lang="scss">
#creation {
  padding: 50px 0 100px 0;
  background-color: white;

  .details {
    width: 80%;
    margin: 30px auto;
    font-size: 1.1rem;
  }

  h1 {
    text-align: center;
    font-size: 1.8rem;
    text-shadow: 2px 3px 3px rgba(0, 0, 0, 0.4);
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