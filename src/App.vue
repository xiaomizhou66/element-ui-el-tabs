<template>
  <div id="app">
    <!-- 左侧导航 -->
    <lefetnav></lefetnav>
    <!-- 右侧购物区 -->
    <div class="main">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import lefetnav from '@/components/commonvue/leftnav'
export default {
  name: 'App',
  components: {
    lefetnav
  }
}

</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /*   margin-top: 60px; */
}
.main{
  float: left;
  width: 95%;
  height: 100%;
  background: rgb(232, 235, 206);
}
</style>
