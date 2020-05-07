<template>
  <div class="story-wrapper">
    <div class="bg"></div>
    <div class="header-wrapper">
      <page-header></page-header>
    </div>

    <div class="story-text-wrapper">
      <div class="story-text">
        <div>外出自粛を守るため</div>
        <div>引きこもり続けたぼく。</div>
        <br>
        <div>しかしその長さから</div>
        <div>彼女である日本酒が</div>
        <div>尽きてしまう。</div>
        <br>
        <div>友達の甲種焼酎と</div>
        <div>ウォッカが残った自宅。</div>
        <br>
        <div>――何も起こらないわけが</div>
        <div>なかった。</div>
        <br>
        <div>彼女との時を</div>
        <div>取り戻すために、</div>
        <div>危険な世界へと</div>
        <div>足を踏み出す……。</div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue';
  import PageHeader from "~/components/PageHeader.vue";

  export default Vue.extend({
    name: "story",
    components: {PageHeader}
  });
</script>

<style scoped lang="scss">
  @import "~assets/colors.scss";

  @keyframes alcoholWars {
    from {
      transform: rotate3d(1, 0, 0, 60deg) translate3d(0, 0, -750px);
    }

    to {
      transform: rotate3d(1, 0, 0, 60deg) translate3d(0, 0, 2500px);
    }
  }

  .bg {
    position: fixed;
    height: 100vh;
    width: 100vw;
    background: repeat center/cover url("/bg_uchu_space.jpg");
    z-index: -1;
  }

  .header-wrapper {
    background: rgba($base-color, 0.3);
  }

  .story-wrapper {
    width: 100vw;
    height: 100vh;
    overflow: hidden;
  }

  .story-text-wrapper {
    height: 100%;
    color: $base-color;
    font-size: 70px;
    letter-spacing: 10px;
    line-height: 2em;
    text-align: center;
  }

  .story-text {
    width: 1500px;
    margin-left: auto;
    margin-right: auto;
    animation: 60s ease-out 500ms both alcoholWars;
  }
</style>
