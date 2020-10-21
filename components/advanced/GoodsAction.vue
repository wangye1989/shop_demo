<template>
  <div id="goods-bottom-bar">
    <button class="goods-action-button" id="add-shopping-car">加入购物车</button>
    <button class="goods-action-button" id="buy-now">立即购买</button>
  </div>
</template>

<script>
export default {

}
</script>

<style>
#goods-bottom-bar{
  background-color: var(--c-f-main);
  border-top: 1px solid var(--c-f-divider);
  padding: 8px 16px;
  height: 56px;
  display: flex;
  justify-content: space-between;
}
#add-shopping-car {
  color: var(--c-f-action);
  border: 1px solid var(--c-f-action);
  background-color: var(--c-f-main);
}
#buy-now{
  color: #fff;
  background-color: var(--c-f-action);
  border: 1px solid var(--c-f-action);
  margin-left: 16px;
  box-shadow: 0 2px 8px rgba(249, 68, 93, 0.25);
}
.goods-action-button {
  font-size: 16px;
  font-weight: 500;
  border-radius: 12px;
  width: 50%;
  height: 100%;
}
</style>