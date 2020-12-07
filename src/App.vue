<template>
  <div id="app">
    <router-view></router-view>
    <main-tab-bar />
  </div>
</template>

<script>
import MainTabBar from '@/components/content/tabbar/MainTabBar.vue'
export default {
  components: {
    MainTabBar
  }
}
</script>
<style lang="less">
@import "./assets/css/base.css";
</style>
