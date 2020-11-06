<template>
  <div class="tabbaritem" @click="itemclick">
<div v-if="!isActive"><slot name="item-icon"></slot></div>
<div v-else><slot name="item-icon-active"></slot></div>
<div :style="activeStyle"><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name : "TabBarItem",
  props : {
    path : String,
    activeColor:{
      // 设置默认字体颜色为红色，如果想改成别的颜色需要再注册的组件标签中配置
      type : String,
      default : 'red'
    }
  },
  computed : {
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle(){
      return this.isActive ? {color : this.activeColor} : {}
    }
  },
  methods : {
    itemclick(){
      this.$router.push(this.path).catch(err => {err})
    }
  }
}
</script>

<style>
.tabbaritem{
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tabbaritem img{
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
  
}
.active{
  color: pink;
}
</style>