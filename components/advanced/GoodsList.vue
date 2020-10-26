<template>
  <div class="goods-list">
    <GoodsCard />
    <GoodsCard />
    <GoodsCard />
    <GoodsCard />
    <GoodsCard />
    <GoodsCard />
  </div>
</template>

<script>
export default {};
</script>

<style>
.goods-list {
  padding: 0 8px;
  display: grid;
  grid-template-rows: 0.5fr 0.5fr;
  grid-template-columns: 0.5fr 1fr;
  grid-gap: 8px;
}
</style>