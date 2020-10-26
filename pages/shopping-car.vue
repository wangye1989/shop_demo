<template>
  <div>
    <div class="nav-topbar">
      <TopbarLargeTitle 
      :title = "topbarTitle"
      :action = "editCar"
      />
    </div>

    <div class="nav-bottombar">
      <CarTotalBar />
      <BottomBar 
      :selected = "2"
      class="no-shadow"
      />
    </div>
  </div>
</template>

<script>
import TopbarLargeTitleVue from '../components/TopbarLargeTitle.vue'
export default {
  data(){
    return {
      topbarTitle : "购物车",
      editCar : "编辑",
    }
  },
}
</script>

<style>

body{
  background-color: var(--c-f-bgcolor);
}
</style>