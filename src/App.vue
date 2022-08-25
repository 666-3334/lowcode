<template>
  <div id="app">
    <router-view/>
  </div>
</template>
<script>
export default {
  mounted(){
    //监听浏览器窗口变化
    window.onresize = ()=>{
      // console.log(document.documentElement.clientWidth);
    }
  }
}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // color: #2c3e50;
  width: 100%;
  height: 100%;
}

</style>
