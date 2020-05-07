<template>
  <div class="container">
    <div class="initialize-view animate__animated animate__fadeIn">
      <img src="/title.png">
    </div>
    <div class="main-view animate__animated animate__fadeInUp animate__delay-4s">
      <div class="main-view--background"></div>
      <the-index-header></the-index-header>
      <main class="main-view-core">
        <h1>酒、明日買いに行きます。</h1>
        <p class="core-text">近日公開予定！</p>
        <p class="info"><small>※情勢の変化により予定が変更になる可能性があります。なお、現在は制作の予定がありません。</small></p>
      </main>
    </div>
  </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import TheIndexHeader from "~/components/TheIndexHeader.vue";

  export default Vue.extend({
    components: {TheIndexHeader}
  })
</script>

<style lang="scss">
  @import "~assets/colors.scss";

  .container {
    min-height: 100vh;
    background: $base-color;
    overflow: hidden;
  }

  .initialize-view {
    width: 100vw;
    height: 100vh;
    position: fixed;
    background: $base-color;
    animation: 500ms fadeOut 3.5s forwards;
  }

  .initialize-view > img {
    height: 93px;
    width: 825px;
    margin: auto;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }

  .main-view {
    width: 100vw;
    height: 100vh;
    background: lighten($theme-color-light, 30);
  }

  .main-view-core {
    display: flex;
    flex-direction: column;
    justify-content: center;
    width: 825px;
    margin-right: auto;
    margin-left: auto;
    margin-top: 240px;
  }

  .main-view-core > h1 {
    background: url("/title.png");
    font-size: 0;
    width: 825px;
    height: 93px;
  }

  .core-text {
    font-size: 32px;
    text-align: center;
    margin-top: 16px;
  }

  .info {
    text-align: center;
  }

  .main-view--background {
    position: absolute;
    height: 100vh;
    width: 100vw;
    background: no-repeat center/cover url("/sake_bg.jpg");
    z-index: -1;
    filter: blur(5px) grayscale(80%) opacity(50%);
  }
</style>
