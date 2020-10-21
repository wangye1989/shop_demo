<template>
  <div class="goods-card">
    <nuxt-link to="/goods/detail">
      <div class="cover">
        <img :src="goodsImage" alt="" />
      </div>
      <div class="des-content">
        <div class="goods-title">{{goodsTitle}}</div>
        <div class="price">${{goodsPrice}}</div>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  props:{
    goodsImage: {
      type: String,
      default: "http://via.placeholder.com/350x350",
    },
    goodsTitle: {
      type: String,
      default: "商品标题可能会比较长，内容过长还需要换行",
    },
    goodsPrice:{
      type: String,
      default: "444",
    },
  }
};
</script>

<style>
.goods-card {
  position: relative;
  background-color: var(--c-f-main);
  border-radius: 6px;
  overflow: hidden;
  box-shadow: 0 0 1 rgba(0, 0, 0, 0.1);
}
.cover {
  width: 100%;
  height: 160px;
  overflow: hidden;
}
.cover img{
  display: block;
  min-width: 100%;
  min-height: 100%;
}
.des-content {
  padding: 8px;
}
.goods-title {
  font-size: 16px;
  line-height: 22px;
  color: var(--c-t-primary);
  margin-bottom: 4px;
}
.price {
  font-size: 18px;
  font-weight: 800;
  line-height: 24px;
  color: var(--c-f-action);
}
</style>