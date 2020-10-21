<template>
  <div class="SearchBar">
    <input class="search" type="text" placeholder="搜索商品名称" />
  </div>
</template>

<script>
export default {};
</script>

<style>
.SearchBar {
  height: 56px;
  padding: 10px 16px;
  background-color: var(--c-f-main);
  border-bottom: 1px solid var(--c-f-divider);
}
.search {
  border-radius: 12px;
  background-color: var(--c-f-bgcolor);
  height: 36px;
  width: 100%;
  padding: 12px;
  font-size: 16px;
  line-height: 36px;
  color: var(--c-t-primary);
}
</style>