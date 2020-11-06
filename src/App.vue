<template>
  <div id="app">
    <router-view></router-view>
    <MainTabBar></MainTabBar>
  </div>
</template>

<script>
import MainTabBar from './components/MainTabbar/MainTabBar'
export default {
  name : 'App',
  components : {
    MainTabBar
  }
}
</script>
<style>
/* @import './assets/css/normalize.css' */

</style>
