<template>
  <div id= "goods-detail-topbar">
    <div class="back-icon" @click="goback">
      <i class="ri-arrow-left-line icon-size-24"></i>
    </div>
    <div class="more-icon">
      <i class="ri-share-forward-line icon-size-24"></i>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    goback(){
      this.$router.go(-1)
    }
  }
}
</script>

<style>

#goods-detail-topbar{
  display: flex;
  flex-flow: row;
  justify-content: space-between;
  padding: 8px 16px 0px 16px;
  height: 56px;
}

.back-icon, .more-icon {
  border-radius: 50%;
  background-color: rgba(0, 0, 0, .8);
  width: 48px;
  height: 48px;
  padding: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, .2);
  transition: all 0.35s;
}
.back-icon:active, .more-icon:active {
  background-color: rgba(0, 0, 0, 1);
  box-shadow: 0 0px 0px rgba(0, 0, 0, 0);
}

.back-icon i, .more-icon i{
  color: #fff;
}
</style>