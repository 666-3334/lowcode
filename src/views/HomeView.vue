<template>
  <div class="home">
    <top-view></top-view>
    <div class="content">
      <left-view @addComponent="addComponent"></left-view>
      <center-view :componentIndex='components' @emitComponent='emitComponent'></center-view>
      <right-view :compIndex='compIndex'></right-view>
    </div>
  </div>
</template>

<script>
import TopView from './TopView.vue'
import LeftView from './LeftView.vue'
import RightView from './RightView.vue'
import CenterView from './CenterView.vue'
export default {
  name: 'HomeView',
  data() {
    return {
      components:[],
      compIndex:-1
    }
  },
  components:{
    TopView,
    LeftView,
    RightView,
    CenterView
  },
  methods:{
    addComponent(e){
      console.log(e);
      this.components.push(e)
    },
    emitComponent(){
      console.log('edit');
      this.compIndex = 0
    }
  }
}
</script>
<style lang="less" scoped>
.home {
  width: 100%;
  height: 100%;
  .content {
    width: 100%;
    display: flex;
    justify-content: space-around;
  }
}
</style>
