<template>
  <div>
    <div class="empty">
      <div class="empty-content">
        <div class="help-infor">空空如也</div>
        <div class="help-infor">购物车中没有商品</div>
        <button class="to-buy no-border">再去逛逛</button>
      </div>
    </div>

  </div>
</template>

<script>
export default {

}
</script>

<style>
.help-infor{
  font-size: 24px;
  line-height: 36px;
  font-weight: 800;
  color: var(--c-f-main);
}
.to-buy{
  font-size: 16px;
  line-height: 22px;
  font-weight: 800;
  padding: 12px 32px;
  margin-top: 12px;
  background-color: var(--c-t-primary);
  color: #fff;
  border-radius: 4px;
  box-shadow: 0 4px 24px rgba(250, 90, 165, 0.3);
}
.empty-content {
  position: absolute;
  top: 30%;
  left: 32px;
  /* display: flex; */
  /* flex-flow: column; */
  /* justify-content: start; */
}
.empty{
  position: relative;
  height: 340px;
  /* background-color: var(--c-f-main); */
  /* border-bottom: 1px solid var(--c-f-divider); */
}

body{
  background-color: var(--c-f-action);
}
</style>