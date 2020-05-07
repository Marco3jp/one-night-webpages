<template>
  <div class="animate__animated animate__fadeIn">
    <div class="bg"></div>
    <page-header></page-header>

    <main class="main-content">
      <article-content v-for="(character,index) in characters"
                       :name="character.name"
                       :descriptions="character.descriptions"
                       :label="character.label"
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
    name: "character",
    components: {PageHeader, ArticleContent},
    data: function () {
      return {
        characters: [{
          name: "ぼく",
          label: "主人公",
          descriptions: [
            "日本酒が彼女で軽度のアルコール中毒。日本酒が彼女で軽度のアルコール中毒。",
            "週に5日ほど、酔いがしっかり回る程度に飲み、軽く飲むという発想はないらしい。",
            "とりあえずこの騒動の元凶であり、浮気性との疑いもある。"
          ]
        }, {
          name: "日本酒",
          label: "ぼくの彼女",
          descriptions: [
            "一度開けると早めに飲みたくなってしまうとの理由でぼくから一升瓶で買ってもらえたことがない。",
            "そろそろぼくくんが浮気をしそうな様子に気が付き始めている。",
            "とはいえ単価が高く、他の娘と比べると賞味期限が短いことに負い目を感じているのか、追求できていない。"
          ]
        }, {
          name: "缶チューハイ",
          label: "トラップガール",
          descriptions: [
            "誰にでも（ｒｙで有名な娘。もちろんぼくも飲ませてもらった。",
            "様々な表情で魅了してくるのがずるい。大体が飲みやすい。",
            "様々なお店で購入することができる点から、ワンナイトをしがち。"
          ]
        }, {
          name: "甲種焼酎",
          label: "気になる娘その１",
          descriptions: [
            "安価でオリジナルチューハイを作るのに便利な娘。",
            "蒸留酒にしては度数が低めなので、キンミヤ派とタカラ派がいるはず。多分。",
            "様々な組み合わせをプレイするだけで体が暖かくなってくる。当たり前だろアルコールなんだぞ。"
          ]
        }, {
          name: "（ピュア）ウォッカ",
          label: "気になる娘その２",
          descriptions: [
            "安価でオリジナルカクテル？を作るのに便利な娘。",
            "度数はものによるので、割る相手に合わせて調節したりできる。",
            "王道のプレイからオリジナルのプレイまで、体を温めるのに最適。当たり前だろ北の世界で生まれてるんだぞ。"
          ]
        }, {
          name: "乙種焼酎",
          label: "クセのある娘",
          descriptions: [
            "好みが分かれると思われる娘だけど、奥の深さがクセになる。",
            "ロックはもちろん、水割りやソーダ割り、お湯割りなど楽しみ方のバリエーションが豊富。",
            "親麦や芋はもちろんしそや米など幅広い。"
          ]
        }, {
          name: "ビール",
          label: "アルコールのトップアイドル",
          descriptions: [
            "長きに渡って外食の女王として圧倒的な存在感を見せていて、看板娘としても活躍している。",
            "味わいは少しビターで、媚を売らない姿勢にハートを撃ち抜かれてしまう。",
            "あくまでアイドルとぼくたちという距離感から近づくことはないが、ガチ恋勢が多いことで有名。"
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
