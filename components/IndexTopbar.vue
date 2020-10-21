<template>
  <div class="index-topbar">
    <div class="home-title">
      <div id="home-title">SHOPPING</div>
      <div class="switch-app">
        <i class="ri-arrow-left-right-line" id="switch-icon"><span id="switch-text">切换</span></i>
        </div>
      </div>
    <div class="home-search">
      <input class="input-search" type="text" placeholder="搜索商品" />
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.index-topbar {
  position: relative;
  background-color: var(--c-f-main);
  border-bottom: var(--c-f-divider);
}
.switch-app {
  position: absolute;
  top: 12px;
  right: 16px;
  display: flex;
  justify-items: center;
  padding: 8px 16px;
  align-items: center;
  background-color: var(--c-f-bgcolor);
  border-radius: 8px;
}
.home-title {
  display: flex;
  justify-content: space-between;
  flex-flow: row;
  margin: 8px 0 ;
}
#home-title {
  font-size: 24px;
  font-weight: 800;
  padding-left: 16px;
  height: 48px;
  line-height: 48px;
  color: var(--c-t-primary);
}
#switch-icon {
  color: #FF6177;
  background-color: var(--c-f-bgcolor);
  font-size: 14px;
}
#switch-text {
  color: var(--c-f-action);
}
.home-search{
  padding: 4px 16px 8px 16px;
}
.input-search {
  border-radius: 12px;
  background-color: var(--c-f-bgcolor);
  border: none;
  height: 44px;
  width: 100%;
  padding: 12px;
  font-size: 16px;
  line-height: 36px;
  color: var(--c-t-primary);
}
</style>