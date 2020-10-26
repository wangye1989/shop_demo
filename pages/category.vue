<template>
  <div>
      <div class="nav-topbar">
        <SearchBar/>
      </div>

      <!-- 菜单的左右结构布局 -->
      <div class="menu-list">
          <div class="type-menu" >
            <!-- todo：默认选中状态，点击切换选中状态 -->
        <div  class="menu-item"   v-for="(item, key) in menu" :key="key" :class="{'menu-selected': activeKey == key}"  @click="update(key)">{{item.menuTitle}}</div>
      </div>

      <!-- 菜单内容 -->
        <div class="categry-content">
          <div class="categry-item" v-if="menu[activeKey]" v-for="(itemType, index) in menu[activeKey].list" :key="index">
            <img class="categry-img" :src="itemType.lableImg" />
            <div class="categry-name">{{itemType.lableTitle}}</div>
          </div>
        </div>
      </div>
      <div class="nav-bottombar">
        <BottomBar
        :selected = "1"
        />
      </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeKey : 0,
      menu:[
      {menuTitle:'男装',
      list:[
        {lableImg:'http://via.placeholder.com/100',lableTitle:'男装-1'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'男装-2'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'男装-3'},
      ]},
      {menuTitle:'女装',
      list:[
        {lableImg:'http://via.placeholder.com/100',lableTitle:'女装-1'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'女装-2'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'女装-3'},
      ]},
      {menuTitle:'化妆品',
      list:[
        {lableImg:'http://via.placeholder.com/100',lableTitle:'化妆品-1'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'化妆-2'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'化妆-3'},
      ]},
      {menuTitle:'数码科技',
      list:[
        {lableImg:'http://via.placeholder.com/100',lableTitle:'手机'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'电脑'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'键盘'},
        {lableImg:'http://via.placeholder.com/100',lableTitle:'显示器'},
      ]},
    ],
    }
  },

  methods:{
    update(key){
      this.activeKey = key;
    }
  },
}
</script>

<style>

.search-bar {
  position: fixed;
  top: 0px;
  z-index: 999;
  width: 100%;
}
.menu-list {
  display: grid;
  grid-template-columns: 0.5fr 1fr;
  margin-top: 56px;
  background: var(--c-f-main);
}
.type-menu {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: auto;
  background-color: var(--c-f-bgcolor);
}
.menu-item {
  font-size: 16px;
  color: var(--c-t-primary);
  align-items: center;
  padding: 12px 24px;
}
.menu-selected {
  font-size: 16px;
  align-items: center;
  padding: 12px 24px;
  background-color: var(--c-f-main);
  border-left: 2px solid var(--c-f-action);
}
.categry-content{
  background-color: var(--c-f-main);
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 88px 88px;
  gap: 10% 5%;
  padding: 16px 4px;
}
.categry-item {
  display: flex;
  flex-flow: column;
  align-items: center;
}
.categry-name {
  font-size: 12px;
  line-height: 24px;
  font-weight: 700;
  color: var(--c-t-primary);
}
.categry-img{
  width: 64px;
  height: 64px;
  background-color: #e0e0e0;
}

body{
  background-color: var(--c-f-bgcolor);
}
</style>