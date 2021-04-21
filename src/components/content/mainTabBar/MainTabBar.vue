<template>
  <tab-bar>
    <tab-bar-item path="/home" activeColor="blue">
      <img slot="item-icon" src="~assets/img/TabBar/home.svg"/>
      <img slot="item-icon-active" src="~assets/img/TabBar/home-active.svg"/>
      <div slot="item-text">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category" activeColor="blue">
      <img slot="item-icon" src="~assets/img/TabBar/category.svg"/>
      <img slot="item-icon-active" src="~assets/img/TabBar/category-active.svg"/>
      <div slot="item-text">分类</div>
    </tab-bar-item>
    <tab-bar-item path="/cart" activeColor="blue">
      <img slot="item-icon" src="~assets/img/TabBar/cart.svg"/>
      <img slot="item-icon-active" src="~assets/img/TabBar/cart-active.svg"/>
      <div slot="item-text">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile" activeColor="blue">
      <img slot="item-icon" src="~assets/img/TabBar/profile.svg"/>
      <img slot="item-icon-active" src="~assets/img/TabBar/profile-active.svg"/>
      <div slot="item-text">个人</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from "components/toolBar/TabBar";
  import TabBarItem from "components/toolBar/TabBarItem";
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
