<template>
  <div class="animate__animated animate__fadeIn">
    <div class="bg"></div>
    <page-header></page-header>

    <main class="main-content">
      <article-content v-for="(location,index) in locations"
                       :name="location.name"
                       :descriptions="location.descriptions"
                       :label="location.label"
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
    name: "location",
    components: {PageHeader, ArticleContent},
    data: function () {
      return {
        locations: [{
          name: "自宅",
          label: "Shelter",
          descriptions: [
            "外出自粛の主戦場となった場所。",
            "後には偉大な戦いを繰り広げられた古戦場として語り継がれていくこととなる。"
          ]
        }, {
          name: "酒屋",
          label: "聖地",
          descriptions: [
            "かけがえのないものがここに在る。",
            "アルコールの煌めきはいつもここに。"
          ]
        }, {
          name: "Amazon",
          label: "部分互換聖地",
          descriptions: [
            "酒屋と部分的に重複する要素があったことで聖地互換だった。",
            "外出自粛を受けて多くの商品が入荷待ちとなる異常事態が起きてしまった。"
          ]
        }, {
          name: "インターネット",
          label: "ここがぼくたちの、アナザーワールド。",
          descriptions: [
            "緊急事態となって以降酷使され続けている場所。",
            "価値が高いとわかった一方で、現実の代わりにはならないこともまたわかり始めてきた。"
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
