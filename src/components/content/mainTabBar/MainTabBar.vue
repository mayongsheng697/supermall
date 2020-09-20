<template>
  <tab-bar>
    <tab-bar-item path="/home" textColor = 'blue'>
      <img slot="item-icon" src="~assets/img/tabbar/主页.png" alt="">
      <img slot="item-active" src="~assets/img/tabbar/4.png" alt="">
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="item-icon" src="~assets/img/tabbar/1.png" alt="">
      <img slot="item-active" src="~assets/img/tabbar/4.png" alt="">
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="item-icon" src="~assets/img/tabbar/购物车-23.png" alt="">
      <img slot="item-active" src="~assets/img/tabbar/4.png" alt="">
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="item-icon" src="~assets/img/tabbar/我的.png" alt="">
      <img slot="item-active" src="~assets/img/tabbar/4.png" alt="">
      <div slot="item-text">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>



<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from "components/common/tabbar/TabBarItem";
export default {
  name: "MainTabBar",
  components:{
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>
