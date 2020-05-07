<template>
  <div class="index-header">
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
</template>

<script lang="ts">
  import Vue from 'vue';

  export default Vue.extend({
    name: "TheIndexHeader"
  });
</script>

<style scoped lang="scss">
  @import '~assets/colors.scss';

  .index-header {
    display: flex;
    height: 60px;
    line-height: 60px;
    justify-content: space-evenly;
  }

  .reset-link-style {
    text-decoration: none;
    color: $font-color;
    font-size: 26px;
  }

  .index-header div {
    width: 240px;
    height: 100%;
    text-align: center;
  }

  .index-header div:hover {
    // キメラってレベルじゃねえぞ
    background: rgba($theme-color, 0.5);
  }
</style>
