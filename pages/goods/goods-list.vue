<template>
  <div>
    <div class="top-area">
      <TopBar 
      :title="title"
      :topBarAction = "topBarAction"
      />
    </div>
    <div class="goods-list-view">
      <GoodsCard
       v-for="(item, index) in list"
       :goodsImage="item.goodsImage"
       :goodsTitle="item.goodsTitle"
       :goodsPrice="item.goodsPrice"
       />
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      title:"商品列表",
      topBarAction : "",
    }
  },
  methods:{
    list:[
        {goodsImage:'http://via.placeholder.com/450',goodsTitle:'这个图片是自定义的图片内容',goodsPrice:'123'},
        {goodsImage:'https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60',goodsTitle:'苹果手机',goodsPrice:'999'},
        {goodsTitle:'图片没传值，使用的是默认值',goodsPrice:'123'},
        {goodsTitle:'文本过多的时候好像有问题，grid不能实现瀑布流',goodsPrice:'123'},
        {goodsPrice:'123'},
        {goodsPrice:'123'},
      ]
  }
};
</script>

<style>
.top-area{
  position: fixed;
  top: 0px;
  width: 100%;
  z-index: 999;
}

body {
  background-color: var(--c-f-bgcolor);
}
.goods-list-view {
  margin-top: 64px;
}

</style>