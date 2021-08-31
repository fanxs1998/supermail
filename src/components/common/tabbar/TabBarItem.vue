<template>
  <div class="tab-bar-item" @click="!isActive && itemClick()">
    <!--默认没选中的图片状态-->
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <!--选中的图片状态-->
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <!--文字-->
    <div >
      <slot name="item-text"></slot>
    </div>
<!--    <img src="../../assets/img/tabbar/homepage.svg" alt="">-->
<!--    <div>首页</div>-->
  </div>
</template>

<script>
  export default {
    name: "TabBarItem",
    props: {
      path: String,
      activeColor: {
        type: String,
        default: 'red'
      }
    },
    data() {
      return {
         // isActive: false
      }
    },
    computed: {
      //当前路由是否活跃
      isActive() {
        return this.$route.path.indexOf(this.path) !== -1
      },
      //当前路由活跃变色
      activeStyle() {
        return this.isActive ? {color: this.activeColor} : {}
      }
    },
    methods: {
      itemClick() {
        this.$router.push(this.path)
      }
    }
  }
</script>

<style scoped>
  
  .tab-bar-item {
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
  }
  
  .tab-bar-item img{
    width: 24px;
    height: 24px;
    margin-top: 3px;
    margin-bottom: 2px;
    vertical-align: middle;
  }
  
  .active {
    color: red;
  }
</style>