<template>
  <div id="toolBar">
    <slot></slot>
  </div>
</template>

<script>
    export default {
        name: "TabBar"
    }
</script>

<style scoped>
  #toolBar{
    display: flex;
    background-color: #f6f6f6;
    position: fixed;
    left:0;
    right:0;
    bottom:0;
    box-shadow: 0px -1px 1px rgba(100,1001,100,.2);
  }
</style>
