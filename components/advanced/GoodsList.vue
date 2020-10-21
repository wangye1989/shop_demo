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
  grid-template-rows: 1fr 1fr;
  grid-template-columns: 1fr 1fr;
  grid-gap: 8px;
}
</style>