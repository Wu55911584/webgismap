<template>
  <div id="app">
    <el-container class="app-Out-Pannel">
  <el-header class="sys-header">一张图项目</el-header>
  <el-container class="app-Content-Pannel">
    <el-aside width="200px" class="sys-menu">左侧菜单</el-aside>
    <el-main class="sys-content">
      <MapView />
    </el-main>
  </el-container>
</el-container>

  </div>
</template>

<script>
import MapView from './components/common/MapView';
export default {
  name: 'App',
  components: {
    MapView,
  },
};
</script>

<style>
html,body,#app {
position: relative;
width: 100%;
height: 100%;
margin: 0;
}
.app-Out-Pannel,
.app-Content-Pannel {
  height: 100%;
}
.sys-header{
  background-color: rgb(102, 102, 219);
  line-height: 60px;
  color: aliceblue;
  font-size: 20px;
}
.sys-menu{
  background-color: #C0C4CC;
}
.sys-content{
  padding: 5px !important;
}
</style>
