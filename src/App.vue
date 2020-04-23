<template>
  <div id="app">
    <div id="nav">
      <Top></Top>
      <Middle></Middle>
      <Bottom></Bottom>
    </div>
    <router-view/>
  </div>
</template>
<script>
  import Top from './components/top'
  import Bottom from './components/bottom'
  import Middle from './components/middle'
  export default {
    name:'app',
    components:{
      Top,
      Bottom,
      Middle
    }
  }
</script>
<style>
  body,html{
    margin: 0;
    padding:0;
    position: relative;
  }
</style>
