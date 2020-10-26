<template>
  <div>
    <div class="wall">
      <div class="username">王也</div>
      <div class="user-des">这是一行描述文字</div>
    </div>

    <div class="list-view-layout">
      <div class="order-area">
        <TitleSection
        style="background-color: #fff;"
        :listTitle = "orderTitle"
        :titleSectionAction = "viewAll"
        />
        <div class="order-menu">
          <div class="order-menu-title"><div class="menu-icon"><i class="ri-bank-card-fill icon-size-32 order-icon"></i></div>待付款</div>
          <div class="order-menu-title"><div class="menu-icon"><i class="ri-mail-send-fill icon-size-32 order-icon"></i></div>待发货</div>
          <div class="order-menu-title"><div class="menu-icon"><i class="ri-truck-fill icon-size-32 order-icon"></i></div>待收货</div>
          <div class="order-menu-title"><div class="menu-icon"><i class="ri-chat-smile-3-fill icon-size-32 order-icon"></i></div>未评价</div>
      </div>
      </div>
      
      <ListItem
      :listItemTitle = "myCollection"
      />
      <ListItem
      :listItemTitle = "myInvitationCode"
      />
      <ListItem
      :listItemTitle = "myAddress"
      />
      <ListItem
      :listItemTitle = "settings"
      /> 
    </div>
      <div class="nav-bottombar">
      <BottomBar
      :selected = "3"
      />
      </div>
  </div>
</template>

<script>
export default {
  data(){
    return{
      myCollection:"我的收藏",
      myInvitationCode : "我的邀请码",
      myAddress : "我的地址",
      settings: "设置",
      orderTitle: "我的订单",
      viewAll : "全部订单",
    }
  },

}
</script>

<style>
.wall {
  position: relative;
  width: 100%;
  height: 160px;
  background-color: linear-gradient(180deg, rgba(0, 0, 0, 0.1) 0%, rgba(0, 0, 0, 0.8) 100%);
  background-image: url(../store/user_wall.svg);
  filter:"progid:DXImageTransform.Microsoft.AlphaImageLoader(sizingMethod='scale')";
  -moz-background-size: 100% auto;
  background-size: 100% auto;
}
.wall::before{
  content: "";
  position: absolute;
  bottom: 0px;
  height: 12px;
  width: 100%;
  background-color: var(--c-f-main);
  border-radius: 8px 8px 0 0 ;
  box-shadow: 0 -4px 32px rgba(0, 0, 0, .3);
}
.username{
  position: absolute;
  left: 16px;
  top: 80px;
  font-size: 24px;
  font-weight: 800;
  color: var(--c-f-main);
  z-index: 1;
}
.user-des{
  position: absolute;
  left: 16px;
  top: 110px;
  font-size: 14px;
  color: var(--c-f-main);
  z-index: 1;
}

.list-view-layout{
  display: grid;
  grid-row-gap: 8px;
  /* margin-top: 16px; */
}
.order-menu{
  display: flex;
  height: 96px;
  justify-content: space-between;
  background-color: var(--c-f-main);
  border-bottom: 1px solid var(--c-f-divider);
  padding: 16px;
}
.menu-icon{
  height: 32px;
  width: 32px;
}
.menu-icon .order-icon {
  color: var(--c-danger-500);
  text-shadow: 0 2px 10px rgba(255, 133, 228, 0.5);
}
.order-menu-title {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  color: var(--c-t-primary);
}

body{
  background-color: var(--c-f-bgcolor);
}
</style>