<template>
  <div id="goods-infor">
    <div class="list-view-layout">
    <div class="infor-group">
      <div class="goods-img"><img src="http://via.placeholder.com/350" alt=""></div>
          <div class="detail-infor">
            <div id="goods-title">商品标题可能会比较长，还需要换行显示</div>
            <div id="price">$444</div>
          </div>
    </div>
      <ListItem 
      :listItemTitle = "selectSku"
      />
      <ListItem 
      :listItemTitle = "deliverPrice"
      />
      <ListItem 
      :listItemTitle = "deliverAddress"
      />
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      selectSku : "选择",
      deliverPrice : "运费价格",
      deliverAddress : "送货地址",
    }
  }
}
</script>

<style>
#goods-infor {
  margin-bottom: 64px;
}
.list-view-layout{
  display: grid;
  grid-row-gap: 8px;
}
.detail-infor{
  background-color: var(--c-f-main);
  border-bottom: 1px solid var(--c-f-divider);
  padding: 16px;
}
#goods-title {
  font-size: 18px;
  font-weight: 500;
  color: var(--c-t-primary);
  margin-bottom: 12px;
}
#price {
  font-size: 24px;
  font-weight: 800;
  color: var(--c-f-action);
}

</style>