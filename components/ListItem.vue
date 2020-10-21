<template>
  <div id="list-label">
    <div class="list-title">{{listItemTitle}}</div>
    <div class="icon-r">
      <i :class="icon" class="icon-size-24"></i>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    listItemTitle: String,
    icon:{
      type: String,
      default: "ri-arrow-right-s-line",
    }
  },
  
}
</script>

<style>
  #list-label {
    position: relative;
    display: flex;
    justify-content: space-between;
    padding:18px 16px;
    margin: 0 16px;
    align-items: center;
    height: 56px;
    border-radius: 12px;
    overflow: hidden;
    background-color: var(--c-f-main);
  }
  .list-title {
    font-size: 16px;
    color: var(--c-t-primary);
  }
</style>