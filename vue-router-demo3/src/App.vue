<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div>
      <button @click="goForward()">Forward</button>
      <button @click="goBack()">Backward</button>
      <button @click="goHome()">Go Home</button>
    </div>
    <div>
      <router-link to="/">Home</router-link>
      |
      <router-link to="/params/123/content title is very good">Params</router-link>
      |
      <router-link to="/goHome">Go Home Redirect</router-link>
      |
      <router-link to="/goParams/1234/content title is very good">Go Params Redirect</router-link>
      |
      <router-link to="/jack">Hi1 Alias jack</router-link>
      |
      <router-link to="/mike">Hi2 Alias mike</router-link>
      |
      <router-link to="/home">已不是坑</router-link>
      |
    </div>
    <transition name="fade" mode="out-in">
      <router-view></router-view>
    </transition>
  </div>
</template>
<script>
  export default {
    name: 'app',
    methods:{
      goBack(){
        this.$router.go(-1);
      },
      goForward(){
        this.$router.go(1);
      },
      goHome(){
        this.$router.push('/');
      }
    }
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
  .fade-enter{
    opacity: 0;
  }
  .fade-enter-active{
    transition: opacity .5s;
  }
  .fade-leave{
    opacity: 1;
  }
  .fade-leave-active{
    opacity: 0;
    transition: opacity .5s;
  }
</style>
