<template>
  <div>
    <h1>{{msg}}-{{$route.params.username}}-{{$route.params.id}}</h1>
  </div>
</template>
<script>
  export default {
    name: 'hi1',
    data () {
      return {
        msg: 'Hi1 Vue'
      }
    }
  }
</script>
<style scoped>
</style>
