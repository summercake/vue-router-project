<template>
  <div>
    <h2>{{msg}}</h2>
    <p>newsId:{{$route.params.newsId}}</p>
    <p>newsTitle:{{$route.params.newsTitle}}</p>
  </div>
</template>
<script>
  export default {
    name: 'Params',
    data(){
      return {
        msg:'Params Page'
      }
    },
    beforeRouteEnter:(to,from,next)=>{
      console.log('Ready to Entry Route')
      next()
    },
    beforeRouteLeave:(to,from,next)=>{
      console.log('Ready to Leave Route')
      next()
    }
  }
</script>
<style scoped>
</style>
