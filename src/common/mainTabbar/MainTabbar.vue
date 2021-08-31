<template>
  <tab-bar>
    <tar-bar-item path="/home" active-color="blue">
      <img slot="item-icon" src="~assets/img/tabbar/homepage.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/homepageactive.svg">
      <div slot="item-text">首页</div>
    </tar-bar-item>
    <tar-bar-item path="/category">
      <img slot="item-icon" src="~assets/img/tabbar/category.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/categoryactive.svg">cannot resolve directory 'tabbar'
      <div slot="item-text">分类</div>
    </tar-bar-item>
    <tar-bar-item path="/cart">
      <img slot="item-icon" src="~assets/img/tabbar/shopcart.svg">
      <img slot="item-icon-active" src="../assets/img/tabbar/shopcartactive.svg">
      <div slot="item-text">购物车</div>
    </tar-bar-item>
    <tar-bar-item path="/profile">
      <img slot="item-icon" src="~assets/img/tabbar/profile.svg">
      <img slot="item-icon-active" src="~assets/img/tabbar/profileactive.svg">
      <div slot="item-text">我的</div>
    </tar-bar-item>
  </tab-bar>
</template>

<script>
  import TabBar from "../../components/common/tabbar/TabBar";
  import TarBarItem from "../../components/common/tabbar/TabBarItem";
  export default {
    name: "MainTabbar",
    components: {TarBarItem, TabBar}
  }
</script>

<style scoped>

</style>