<template>
	<div>
    <h1>{{msg}}</h1>
    <router-view></router-view>
  </div>
</template>
<script>
  export default {
    name: 'Hi',
    data(){
      return {
        msg:'Hi Vue'
      }
    }
  }
</script>
<style scoped>
</style>
