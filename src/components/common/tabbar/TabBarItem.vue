<template>
  <div class='tar-bar-item'
       @click='itemClick'>
    <!-- 外层包装插槽 -->
    <div v-if='!isActive'>
      <slot name='item-icon'></slot>
    </div>
    <div v-else>
      <slot name='item-icon-active'></slot>
    </div>
    <!-- <div :class='{active:isActive}'> -->
    <div :style='activeStyle'>
      <slot name='item-text'></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'coral'
    }
  },
  data () {
    return {
      // isActive: false
    }
  },
  computed: {
    isActive: {
      get () {
        return (this.$route.path.indexOf(this.path) !== -1)
      },
      set () {

      }
    },
    activeStyle: {
      get () {
        return this.isActive ? { color: this.activeColor } : {}
      },
      set () {

      }
    }
  },
  methods: {
    itemClick () {
      this.isActive = !this.isActive
      this.$router.push(this.path)
    }
  }
}
</script>

<style scoped>
.tar-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tar-bar-item img {
  width: 24px;
  height: 24px;
  vertical-align: middle;
  margin-bottom: 2px;
  margin-top: 3px;
}
/* .active {
  color: red;
} */
</style>
