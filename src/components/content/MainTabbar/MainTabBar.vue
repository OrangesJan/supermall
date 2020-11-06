<template>
  <TabBar>
      <TabBarItem path="/home" >
        <img slot="item-icon" src="@/assets/img/1.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/1_active.png" alt="">
        <div slot="item-text">首页</div>
      </TabBarItem>
      <TabBarItem path="/category">
        <img slot="item-icon" src="@/assets/img/2.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/2_active.png" alt="">
        <div slot="item-text">分类</div>
      </TabBarItem>
      <TabBarItem path="/cart">
        <img slot="item-icon" src="@/assets/img/3.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/3_active.png" alt="">
        <div slot="item-text">购物车</div>
      </TabBarItem>
      <TabBarItem path="/profile">
        <img slot="item-icon" src="@/assets/img/4.png" alt="">
      <img slot="item-icon-active" src="@/assets/img/4_active.png" alt="">
        <div slot="item-text">我的</div>
      </TabBarItem>
    </TabBar>
</template>

<script>

import TabBar from '../../common/Tabbar/TabBar'
import TabBarItem from '../../common/Tabbar/TabBarItem'
export default {
  name : "MainTabBar",
  components : {
    TabBar,
    TabBarItem
  }
}
</script>

<style>

</style>