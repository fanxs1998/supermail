<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">首页</div> </nav-bar>

    <home-swiper :banners="banners"/>
  </div>
</template>

<script>
  import NavBar from "components/common/navbar/NavBar";
  import HomeSwiper from "./childComponents/HomeSwiper";
  
  import {getHomeMultidata} from "api/home"
  
  export default {
    name: "Home",
    components: {
      NavBar,
      HomeSwiper
    },
    
    data() {
      return {
        banners: [],
        recommend: []
      }
    },
    
    created() {
      getHomeMultidata().then(res => {
        console.log(res);
        this.banners = res.data.banner.list
        this.recommends = res.data.recommends
        console.log(this.banners);
      })
    }
  }
</script>

<style scoped>
  .home-nav {
    background-color: var(--color-tint);
    color: #fff;
  }
</style>