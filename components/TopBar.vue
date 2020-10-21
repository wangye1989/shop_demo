<template>
  <div class="topbar">
    <div class="icon-l" style="top:16px;" @click="goback">
      <i :class="icon" class="icon-size-24"></i>
    </div>
    <div id="title">{{ title }}</div>
    <div class="action">{{topBarAction}}</div>
  </div>
</template>

<script>
export default {
  props:{
    title:String,
    topBarAction: String,
    icon:{
      type: String,
      default: "ri-arrow-left-s-line",
    },
  },
  methods: {
    goback(){
      this.$router.go(-1)
    }
  }
};
</script>

<style>
.topbar {
  position: relative;
  height: 56px;
  background: var(--c-f-main);
  border-bottom: 1px solid var(--c-f-divider);
}

#title {
  font-size: 18px;
  color: var(--c-t-primary);
  text-align: center;
  line-height: 56px;
}

.action {
  position: absolute;
  right: 16px;
  top: 16px;
  color: var(--c-f-action);
}
</style>