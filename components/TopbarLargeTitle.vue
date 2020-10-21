<template>
  <div class="large-title">
    <div class="title">{{title}}</div>
    <div class="action" @click="$router.push(url)">{{action}}</div>
  </div>
</template>

<script>
export default {
  props : {
    title : {
      type : String,
      default : "标题",
    },
    action : {
      type : String,
      default : '操作文本',
      url : String,
    },
  }
}
</script>

<style>
.large-title{
  padding: 12px 16px;
  display: flex;
  justify-content: space-between;
  background-color: var(--c-f-main);
  border-bottom: 1px solid var(--c-f-divider);
}
.title {
  font-size: 18px;
  font-weight: 800;
  color: var(--c-t-primary);
}
.action {
  color: var(--c-f-action);
}
</style>