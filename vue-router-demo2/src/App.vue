<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <router-link to="/">Home</router-link>
      <router-link to="/reverse">Reverse</router-link>
    </div>
    <router-view></router-view>
    <router-view name="left" style="float:left;width: 50%;height: 300px;background: gray;"></router-view>
    <router-view name="right" style="float:right;width: 50%;height: 300px;background: pink;"></router-view>
  </div>
</template>
<script>
  export default {
    name: 'App'
  }
</script>
<style>
  #app{
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2C3E50;
    margin-top: 60px;
  }
</style>
