<template>
  <div class="tool-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-active"></slot>
    </div>
    <!--<div :class="{active:isActive}">-->
    <!--<slot name="item-text"></slot>-->
  <!--</div>-->
    <div :style="activeStyle">
      <slot name="item-text"></slot>
    </div>
  </div>
</template>

<script>
    export default {
        name: "TabBarItem",
        data(){
          return {
            // isActive : true
          }
        },
      computed:{
          isActive(){
            return this.$route.path.indexOf(this.path) !== -1
          },
        activeStyle(){
            return this.isActive ? {color:this.activeColor} : {}
        }
      },
      props:{
        path:String,
        activeColor:{
          type:String,
          default:"red"
        }
      },
      methods:{
          itemClick()
          {
            this.$router.replace(this.path)
          }
      }
    }
</script>

<style scoped>
  .tool-bar-item{
    flex:1;
    text-align: center;
    height: 49px;
  }

  .tool-bar-item img{
    width: 24px;
    height: 24px;
  }

  /*.active{*/
    /*color:red;*/
  /*}*/
</style>
