<template>
  <div id='tar-bar'>
    <slot></slot>
  </div>

</template>

<script>
export default {

}
</script>

<style scoped>
#tar-bar {
  display: flex;
  position: fixed;
  left: 0px;
  right: 0px;
  bottom: 0px;
  background: #f6f6f6;
  box-shadow: 0px -3px 2px rgba(100, 100, 100, 0.2);
}
</style>
