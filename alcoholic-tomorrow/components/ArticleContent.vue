<template>
  <div class="content">
    <h2>{{name}}</h2>
    <p class="label">{{label}}</p>
    <div class="descriptions">
      <p v-for="description in descriptions">{{description}}</p>
    </div>

  </div>
</template>

<script lang="ts">
  import Vue from 'vue';

  export default Vue.extend({
    name: "ArticleContent",
    props: ['name', 'label', 'descriptions']
  });
</script>

<style scoped lang="scss">
  @import "~assets/colors.scss";

  .descriptions {
    margin-top: 12px;
  }

  .label {
    border-bottom: 3px $theme-color-light double;
    margin-left: 12px;
  }
</style>
