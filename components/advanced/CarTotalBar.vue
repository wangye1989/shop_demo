<template>
  <div class="total-bar-layout">
    <div class="select-all">
      <div id="select-icon">
        <i :class="icon" class="icon-size-24"></i>
      </div>
      <div id="select-text">全选</div>
    </div>

    <div class="action-content">
      <div id="all-text">合计</div>
      <div id="total-price">$1234</div>
      <button id="buy-btn">结算</button>
    </div>
  </div>
</template>

<script>
export default {
  porps: {
    icon: {
      type: String,
      default: "ri-checkbox-blank-circle-line",
    },
  },
}
</script>

<style>
.total-bar-layout {
  position: relative;
  display: flex;
  height: 48px;
  justify-content: space-between;
  justify-items: center;
  padding: 4px 16px;
  background-color: rgba(255, 255, 255, .7);
  border-top: 1px solid var(--c-f-divider);
  z-index: 9999;
}
.total-bar-layout::before{
  content: "";
  position: absolute;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  backdrop-filter: blur(10px);
  z-index: -1;
}
.select-all{
  display: flex;
  align-items: center;
}
.action-content {
  /* position: absolute; */
  align-items: center;
  right: 16px;
  display: flex;
  right: 16px;
}
#select-icon{
  height: 24px;
  width: 24px;
}
#select-text{
  font-size: 14px;
  line-height: 30px;
  margin-left: 4px;
}
#all-text {
  font-size: 14px;
  line-height: 30px;
}
#total-price{
  font-size: 18px;
  font-weight: 800;
  color: var(--c-f-action);
  line-height: 30px;
  margin-left: 8px;
}
#buy-btn {
  background-color: var(--c-f-action);
  border: none;
  border-radius: 8px;
  padding: 8px 24px;
  color: #fff;
  font-size: 16px;
  line-height: 16px;
  margin-left: 8px;
  box-shadow: 0 2px 8px rgba(249, 68, 93, 0.25);
}
</style>