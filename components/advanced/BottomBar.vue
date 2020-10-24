<template>
  <div id="bottom-bar">
    <BottomBarItem v-for="(item, index) in list"
    :key="index"
    :class="{'choosed': selected === index}"
    :lable = "item.title"
    :url = "item.url"
    :icon = "item.icon"

    />
  </div>
</template>

<script>
export default {
  props: {
    selected: {
      type: Number,
      default: 0
    }
  },
  data() {
    return {
      list: [
        { title: '', url: '/' , icon : "ri-home-3-line"},
        { title: '', url: '/category' ,icon : "ri-function-line"},
        { title: '', url: '/shopping-car',icon : "ri-shopping-cart-2-line" },
        { title: '', url: '/user' ,icon : "ri-user-3-line" }
      ],
    }
  },
};
</script>

<style>
#bottom-bar {
  z-index: 998;
  display: flex;
  justify-content: space-between;
  padding: 12px 24px;
  height: 56px;
  background-color: rgba(255, 255, 255, .7);
  width: 100%;
  box-shadow: 0 0 4px rgba(0, 0, 0, .06);
}
#bottom-bar::before{
  content: "";
  position: absolute;
  top: 0px;
  bottom: 0px;
  left: 0px;
  right: 0px;
  backdrop-filter: blur(10px);
  z-index: -1;
}

.bottom-bar .choosed {
  color: var(--c-f-action) !important;
}
</style>