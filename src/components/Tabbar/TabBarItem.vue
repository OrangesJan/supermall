<template>
  <div class="tabbaritem" @click="itemclick">
<div v-if="!isActive"><slot name="item-icon"></slot></div>
<div v-else><slot name="item-icon-active"></slot></div>
<div><slot name="item-text"></slot></div>
  </div>
</template>

<script>
export default {
  name : "TabBarItem",
  props : {
    path : String
  },
  computed : {
    isActive(){
      return this.$route.path.indexOf(this.path) !== -1
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