<template>
  <div class="center-view">
    <h3>页面效果</h3>
    <div class="center-content">
      <actual-comp v-for="(item,index) in componentIndex" :key="index" :compIndex='parseInt(item)' @clickComp="edit"></actual-comp>
    </div>
  </div>
</template>

<script>
import ActualComp from '../components/ActualComp.vue'
export default {
  data() {
    return {
      componentArray:[],
      clickTimes:0
    }
  },
  components:{
    ActualComp
  },
  props:{
    componentIndex:{
      type:Array
    }
  },
  watch:{
    componentIndex(newVal){
      console.log(newVal);//string
      this.componentIndex = newVal
      this.componentIndex.forEach(e=>{
        console.log(e);
      })
    }
  },
  methods:{
    updateComponentArray(e){
      this.componentArray.push(e)
    },
    edit(e){
      console.log(e);
      this.clickTimes ++;
      setTimeout(() => {
        this.clickTimes --
      }, 500);
      if(this.clickTimes == 2){
        console.log('twice');
        this.$emit('emitComponent')
      }
    }
  }
}

</script>
<style scoped lang='less'>
.center-view {
    width: 45%;
    height: 500px;
    background-color: #feff;
    h3 {
      width: 100%;
      height: 30px;
      line-height: 30px;
      text-align: center;
    }
}
</style>