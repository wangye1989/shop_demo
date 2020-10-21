<template>
  <div>
    <div class="nav-topbar">
      <IndexTopbar/>
      <!-- <TopBar 
      :title="title"
      class="no-border"
      />
      <SearchBar /> -->
    </div>
    <div class="index-list-view">
      <IndexBanner />
      <TitleSection 
      :listTitle = "listTitle"
      :titleSectionAction = "titleSectionAction"
      />

      <div class="goods-list">
       <GoodsCard
       v-for="(item, index) in list"
       :goodsImage="item.goodsImage"
       :goodsTitle="item.goodsTitle"
       :goodsPrice="item.goodsPrice"
       />
      </div>

    </div>

    

    <div class="nav-bottombar">
      <BottomBar />
    </div>
  </div>
</template>

<script>
export default {
  transitions:"test",
  data(){
    return {
      title: "高端商城",
      listTitle:"热门商品",
      titleSectionAction: "查看更多",
      list:[
        {goodsImage:'http://via.placeholder.com/450',goodsTitle:'这个图片是自定义的图片内容',goodsPrice:'123'},
        {goodsImage:'https://images.unsplash.com/photo-1511707171634-5f897ff02aa9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60',goodsTitle:'苹果手机',goodsPrice:'999'},
        {goodsTitle:'图片没传值，使用的是默认值',goodsPrice:'123'},
        {goodsTitle:'文本过多的时候好像有问题，grid不能实现瀑布流',goodsPrice:'123'},
        {goodsPrice:'123'},
        {goodsPrice:'888'},
      ],
    }
  },

  methods:{

  },

  created() {
    console.log('created');
  }
};
</script>

<style>
body {
  background-color: var(--c-f-bgcolor);
}
/* 创建一个 no-border 样式，覆盖 topbar 组件中的 border 样式 */


.top-area {
  position: fixed;
  top: 0px;
  width: 100%;
  display: block;
  z-index: 999;
}
.index-list-view {
  margin-top: 120px;
  margin-bottom: 73px;

}
.goods-list{
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 8px;
  padding: 0 8px;
}

</style>
