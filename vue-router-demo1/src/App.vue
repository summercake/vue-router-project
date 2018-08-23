<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <router-link to="/">Home</router-link>
      <router-link to="/hi">Hi</router-link>
      <router-link :to="{name:'/hi/hi1',params:{username:'jack', id:'007'}}">Hi1</router-link>
      <router-link to="/hi/hi2">Hi2</router-link>
    </div>
    <router-view></router-view>
    <p>Params : {{$route.name}}</p>
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
