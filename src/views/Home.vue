<template>
  <div>
    <router-view></router-view>
    <main-tab-bar></main-tab-bar>
  </div>
</template>

<script>
  import TabBar from "../components/common/tabbar/TabBar";
  import TarBarItem from "../components/common/tabbar/TabBarItem";
  import MainTabBar from "../components/content/mainTabbar/MainTabBar";
  export default {
    name: "Home",
    components: {
      MainTabBar,
      TarBarItem,
      TabBar
    }
  }
</script>

<style scoped>

</style>