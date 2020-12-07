<template>
  <tab-bar>
    <tab-bar-item v-for='item in TabBarItems'
                  :key='item.text'
                  :path='item.path'>
      <img :src='item.itemIconSrc'
           slot='item-icon'
           alt=''>
      <img :src='item.itemIconActiveSrc'
           slot='item-icon-active'
           alt=''>
      <div slot='item-text'>{{item.text}}</div>
    </tab-bar-item>
    <!-- <tab-bar-item path='/index'>
      <img src='~/assets/img/tabbar/home.svg'
           slot='item-icon'
           alt=''>
      <img src='~assets/img/tabbar/home_active.svg'
           slot='item-icon-active'
           alt=''>
      <div slot='item-text'>首页</div>
    </tab-bar-item>
    <tab-bar-item path='/category'>
      <img src='~assets/img/tabbar/category.svg'
           slot='item-icon'
           alt=''>
      <img src='~assets/img/tabbar/category_active.svg'
           slot='item-icon-active'
           alt=''>
      <div slot='item-text'>分类</div>
    </tab-bar-item>
    <tab-bar-item path='/shopcart'>
      <img src='~assets/img/tabbar/shopcart.svg'
           slot='item-icon'
           alt=''>
      <img src='~assets/img/tabbar/shopcart_active.svg'
           slot='item-icon-active'
           alt=''>
      <div slot='item-text'>购物车</div>
    </tab-bar-item>
    <tab-bar-item path='/profile'>
      <img src='~assets/img/tabbar/profile.svg'
           slot='item-icon'
           alt=''>
      <img src='~assets/img/tabbar/profile_active.svg'
           slot='item-icon-active'
           alt=''>
      <div slot='item-text'>我的</div>
    </tab-bar-item> -->
  </tab-bar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem.vue'

import homeIcon from '@/assets/img/tabbar/home.svg'
import homeActiveIcon from '@/assets/img/tabbar/home_active.svg'
import categoryIcon from '@/assets/img/tabbar/category.svg'
import categoryActiveIcon from '@/assets/img/tabbar/category_active.svg'
import shopcartIcon from '@/assets/img/tabbar/shopcart.svg'
import shopcartActiveIcon from '@/assets/img/tabbar/shopcart_active.svg'
import profileIcon from '@/assets/img/tabbar/profile.svg'
import profileActiveIcon from '@/assets/img/tabbar/profile_active.svg'

export default {
  components: { TabBar, TabBarItem },
  data () {
    return {
      TabBarItems: [
        {
          path: '/index',
          itemIconSrc: homeIcon,
          itemIconActiveSrc: homeActiveIcon,
          text: '首页'
        },
        {
          path: '/category',
          itemIconSrc: categoryIcon,
          itemIconActiveSrc: categoryActiveIcon,
          text: '分类'
        },
        {
          path: '/shopcart',
          itemIconSrc: shopcartIcon,
          itemIconActiveSrc: shopcartActiveIcon,
          text: '购物车'
        },
        {
          path: '/profile',
          itemIconSrc: profileIcon,
          itemIconActiveSrc: profileActiveIcon,
          text: '我的'
        }
      ]
    }
  }
}
</script>

<style scoped>
</style>
