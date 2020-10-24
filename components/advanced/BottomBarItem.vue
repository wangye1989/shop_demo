<template>
  <router-link class="bottom-bar-item" :to="url">
    <div class="bottom-icon">
      <i :class="icon" class="icon-size-32"></i>
    </div>
    <div class="bottom-title">{{lable}}</div>
  </router-link>
</template>

<script>
export default {
  transition: 'test',
  props:{
    lable : String,
    url : String,
    icon : {
      type : String,
      default : "ri-home-3-line",
    },
  },

};
</script>

<style>
.bottom-bar-item {
  display: flex;
  flex-flow: column;
  align-items: center;
}
.bottom-icon {
  width: 32px;
  height: 32px;
  color: var(--c-t-primary);
}
.bottom-icon i {
  text-shadow: 0 2px 6px rgba(0, 0, 0, .1);
}
.bottom-title {
  font-size: 12px;
  font-weight: 16px;
  color: var(--c-t-primary);
}
</style>