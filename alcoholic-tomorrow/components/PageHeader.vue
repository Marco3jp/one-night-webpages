<template>
  <header class="header">
    <nuxt-link to="/" class="reset-link-style">
      <div class="title-link">
      </div>
    </nuxt-link>

    <div class="sub-pages">

      <nuxt-link to="/story" class="reset-link-style">
        <div>
          <span>STORY</span>
        </div>
      </nuxt-link>

      <nuxt-link to="/character" class="reset-link-style">
        <div>
          <span>CHARACTER</span>
        </div>
      </nuxt-link>

      <nuxt-link to="/location" class="reset-link-style">
        <div>
          <span>LOCATION</span>
        </div>
      </nuxt-link>

      <nuxt-link to="/word" class="reset-link-style">
        <div>
          <span>WORD</span>
        </div>
      </nuxt-link>
    </div>
  </header>
</template>

<script lang="ts">
  import Vue from 'vue';

  export default Vue.extend({
    name: "PageHeader"
  });
</script>

<style scoped lang="scss">
  @import "~assets/colors.scss";

  .reset-link-style {
    text-decoration: none;
    color: $font-color;
    font-size: 26px;
  }


  .title-link {
    background: no-repeat center/cover url("/title.png");
    width: 600px;
    height: 60px;
    margin-left: 32px;
  }

  .sub-pages {
    display: flex;
    margin-left: 32px;
    flex-grow: 1;
    justify-content: space-evenly;
  }

  .header {
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    display: flex;
    height: 60px;
    line-height: 60px;
    justify-content: space-between;
    z-index: 10;
  }

  .sub-pages div {
    width: 240px;
    height: 100%;
    text-align: center;
  }


  .sub-pages div:hover {
    background: rgba($theme-color, 0.5);
  }
</style>
