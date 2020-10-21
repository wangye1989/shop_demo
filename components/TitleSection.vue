<template>
  <div class="title-section">
    <div class="title-indicator"></div>
    <div class="title-des">{{listTitle || 'xxx'}}</div>
    <div class="goods-more">
      <nuxt-link to="goods/goods-list">{{titleSectionAction}}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  props :{
    listTitle: {
      type: String,
      default: 'TITLE'
    },
    titleSectionAction: String,
  },
};
</script>

<style>
.title-section {
  position: relative;
  height: 42px;
}
.title-indicator {
  position: absolute;
  left: 0;
  top: 14px;
  background-color: var(--c-f-action);
  height: 14px;
  width: 4px;
}
.title-des {
  position: absolute;
  font-size: 16px;
  font-weight: 700;
  line-height: 42px;
  color: var(--c-t-primary);
  margin-left: 13px;
}
.goods-more {
  position: absolute;
  font-size: 14px;
  font-weight: 400;
  line-height: 42px;
  right: 16px;
  color: var(--c-t-primary);
}
.goods-more a {
  color: var(--c-t-primayr);
}
</style>