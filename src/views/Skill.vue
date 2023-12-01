<template>
  <section id="skill">
    <h1 class="title">Skill</h1>
    <h2>習得/学習している技術スタックの紹介をしています。カーソルを合わせることで、スキルレベルの詳細を確認いただけます。</h2>
    <SlideInLeft>
      <div class="frontend">
        <h1>フロントエンド</h1>
        <div class="skill-section">

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" name="HTML"
            :level=4 text="HTMLの基本的なタグとそれらの特有の属性を理解し、適切なウェブページを構築することができます。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" name="CSS" :level=4
            text="基礎的なプロパティを始め、FlexBoxやPositionを使用したレイアウト調整、MediaQueryを使用したレスポンシブデザイン等様々な知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg"
            name="JavaScript" :level=4
            text="基礎的な構文を始め、DOM操作/非同期処理/アロー関数/npmでのライブラリ管理等、JavaScriptでよく使われる機能の知識も身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vuejs/vuejs-original.svg" name="Vue.js"
            :level=4
            text="OptionsApi/CompositionApiどちらの書き方も学習しており、ライフサイクルフックやコンポーネント等Vue特有の機能を始め、VueRouterやBootStrapVueNext等ライブラリの使用方法も理解しています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg"
            name="BootStrap" :level=4 text="基本プロパティを始め、フォームの作成、row/colを活用したGridレイアウトの構築、内部Sassのカスタマイズ等、幅広い知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/sass/sass-original.svg" name="Sass"
            :level=4 text="CSSのネスト、関数や変数の使用、セレクタの使用等基礎的な知識を身に付けています" />

        </div>
      </div>
    </SlideInLeft>

    <SlideInRight>
      <div class="backend">
        <h1>バックエンド</h1>
        <div class="skill-section">

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" name="PHP" :level=4
            text="変数/関数/クラス/MVC/ミドルウェアなどの基礎概念や、PDOを使ったDB接続、composerを用いたライブラリのインストール等、幅広い知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain.svg" name="Laravel"
            :level=4
            text="MVC/ルーティング/マイグレーション/Blade等基礎的な機能に加え、WebSocketやBroadCast等の概念の理解、RestfulApiの構築等様々な知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" name="Node.js"
            :level=3 text="JSの基礎文法、非同期処理、モジュールの管理、Httpリクエストの受け取りとバリデーションの実装等基礎的な知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/express/express-original.svg"
            name="Exspress" :level=3
            text="基礎をはじめ、セッション管理、フロントエンドとの連携、RestfulApiの構築、モダンなORMの使用、MVCに準ずるディレクト構造の作成等様々な知識を身に付けています。" />

          <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" name="MySQL"
            :level=4 text="CRUD操作をはじめ、テーブル設計、リレーションの定義、主キー/外部キーの設定、様々なORMとの連携等幅広い知識を身に付けています。" />

        </div>
      </div>
    </SlideInRight>

    <SlideInLeft>
      <div class="tool-others">
        <h1>ツール / その他</h1>
        <div class="oowaku">
          <div class="skill-section">

            <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/vscode/vscode-original.svg" name="VsCode"
              :level=5 text="プロジェクトごとの設定の管理、言語やフレームワークに必要な拡張機能の導入、ターミナルを使用したデバッグや開発サーバーの立ち上げ等様々な知識を身に付けています。" />

            <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" name="Git" :level=4
              text="add, commit, push, pull等の基礎的なコマンドやbranch, checkout等のブランチ管理、mergeする際のコンフリクト解決もできます。" />

            <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" name="Github"
              :level=4 text="リポジトリの管理、github上でのpullリクエストやmerge等の管理、オープンソースプロジェクトの閲覧を通した学習等様々な知識を身に付けています。" />

            <SkillBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/windows8/windows8-original.svg"
              name="Windows" :level=5 text="自作PCを2台組んだ経験を生かし、OSのインストールから最適な設定、必須ドライバ/便利なソフトウェアのインストール等様々な知識を身に付けています。" />

          </div>
        </div>
      </div>
    </SlideInLeft>

    <SlideInRight>
      <div class="interest">
        <h1>勉強中</h1>
        <div class="oowaku">
          <div class="skill-section">

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" name="React"
              text="useStateやuseEffect等のライフサイクルフック、コンポーネント化等基礎的な機能の理解をしています。" />

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nextjs/nextjs-original-wordmark.svg"
              name="Next.js" text="Reactの基礎機能に加え、SSRの理解、pagesディレクトリの使用方法、Next.js内でのバックエンドの簡単な実装等知識を身に付けています。" />

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nuxtjs/nuxtjs-original.svg"
              name="Nuxt.js" text="Vue.jsの基礎機能に加え、SSRの理解、pagesディレクトリの使用方法、Vue.jsをより便利に使用する方法など知識を身に付けています。" />

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg"
              name="TailwindCss" text="CSSの基礎知識、BootStrapとの違い、様々なプロパティの理解、ライブラリを使用した拡張等基礎的な知識を身に付けています。" />

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" name="Java"
              text="基礎的な構文や型、DB接続やMVCに準じた簡単なプロジェクトの作成等基礎的な知識を身に付けています。" />

            <StudyBlock icon="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg"
              name="SpringBoot" text="MVCに準じたプロジェクトの作成、追加された様々なアノテーションの理解、RestfulApiの実装、フロントエンドの連携等基礎的な知識を身に付けています。" />

          </div>
        </div>
      </div>
    </SlideInRight>
  </section>
</template>

<script setup lang="ts">
import SlideInLeft from "@/components/SlideInLeft.vue"
import SlideInRight from "@/components/SlideInRight.vue"
import SkillBlock from "@/components/SkillBlock.vue"
import StudyBlock from "@/components/StudyBlock.vue"
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
  background: url("../assets/images/sky.jpg");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;

  @include mq() {
    background-attachment: scroll;
  }

  h2 {
    color: white;
    margin-top: 60px;
    margin-bottom: 60px;
    text-shadow: 2px 3px 3px rgba(0, 0, 0, 0.4);
    color: white;
    width: 80%;
  }

  .title {
    font-size: 2.8rem;
    color: white;
    text-align: center;
    margin-top: 60px;
    text-shadow: 2px 3px 3px rgba(0, 0, 0, 0.4);
  }


  .frontend,
  .backend,
  .tool-others,
  .interest {
    margin-top: 50px;
    @include flexCenter;
    flex-direction: column;

    h1 {
      text-align: center;
      color: white;
      text-shadow: 2px 3px 3px rgba(0, 0, 0, 0.4);
      margin: 10px 0 10px 0;
      border-bottom: 3px solid rgb(30, 30, 30);
    }

    .skill-section {
      max-width: 1400px;
      @include flexCenter;
      flex-wrap: wrap;
      margin: 0 0 30px 0;
    }
  }
}
</style>