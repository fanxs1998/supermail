<template>
  <div>
    <router-view></router-view>
    <main-tab-bar></main-tab-bar>
  </div>
</template>

<script>
  import MainTabBar from "components/content/mainTabbar/MainTabBar";
  export default {
    name: "Home",
    components: {
      MainTabBar,
    }
  }
</script>

<style scoped>

</style>