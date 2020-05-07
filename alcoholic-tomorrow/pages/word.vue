<template>
  <div class="animate__animated animate__fadeIn">
    <div class="bg"></div>
    <page-header></page-header>

    <main class="main-content">
      <article-content v-for="(word,index) in words"
                       :name="word.name"
                       :descriptions="word.descriptions"
                       :label="word.label"
                       :key="index"
      >
      </article-content>
    </main>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue';
  import PageHeader from "~/components/PageHeader.vue";
  import ArticleContent from "~/components/ArticleContent.vue";

  export default Vue.extend({
    name: "word",
    components: {PageHeader, ArticleContent},
    data: function () {
      return {
        words: [{
          name: "緊急事態",
          label: "誰も想像していなかった今日",
          descriptions: [
            "地球上はUFOの力によって制圧されてしまった。",
            "UFOの力に汚染された人類は他の人類をも汚染してしまうという状況に陥っている。",
            "それでも生き延びるための策を人類は講じて耐え忍んでいる。"
          ]
        }, {
          name: "外出自粛",
          label: "出会わなければ、出会えるようになるさ",
          descriptions: [
            "緊急事態を受けて外出を避けるのが最適であると考えた各国政府が打ち出した方針のこと。",
            "いつかの\"普通\"を取り戻すために人類は戦い続ける。",
          ]
        }, {
          name: "アルコール",
          label: "作用させたら勝ち。それはヤツもコレも同じさ。",
          descriptions: [
            "ぼくの物語にとって重要な存在。",
            "緊急事態のストレスを破壊する最強の兵器。",
            "一方で外出自粛のせいもあり、一度の外出で大量に買い込まざるを得ない。"
          ]
        }, {
          name: "飲む・飲ませる, プレイ",
          label: "これは怪文書の始まりだ。",
          descriptions: [
            "正気とは思えんけどこれはなんなんだ（？）",
            "意味深な意味で捉えてくれ。何がだよって思うかもしれないが、俺が一番思ってる。",
            "一晩の勢いでこんなサイトを作ったことが全ての理由だ。"
          ]
        }, {
          name: "古戦場",
          label: "ここが\"あの\"",
          descriptions: [
            "そう、ここが\"あの\"古の戦場なんだ。",
            "緊急事態を切り抜けた未来では、外出自粛をともにした自宅やネットワークなどを示し、『ごくり……こ、ここが噂の島か……』と呼ぶ。",
            "あのスマホRPGで語り継がれる伝説のイベントはそういうことなんだよ……。"
          ]
        }]
      }
    }
  });
</script>

<style scoped lang="scss">
  .bg {
    position: fixed;
    height: 100vh;
    width: 100vw;
    background: no-repeat center/cover url("/sake_bg.jpg");
    z-index: -1;
    filter: blur(5px) grayscale(80%) opacity(50%);
  }

  .main-content {
    width: 800px;
    padding-top: 40px;
    padding-bottom: 120px;
    margin-left: auto;
    margin-right: auto;

    & > div:not(:first-child) {
      margin-top: 40px;
    }
  }
</style>
