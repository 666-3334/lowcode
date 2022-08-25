<template>
  <div class="left-view">
    <h3 class="left-title">组件选择</h3>
    <div class="left-content">
      <default-comp
        v-for="(item, index) in allComponents"
        :key="index"
        :compIndex="index"
        @addComp="addComp"
      ></default-comp>
    </div>
  </div>
</template>

<script>
import DefaultComp from "../components/DefaultComp.vue";
import allComponents from "../components/getAllComps";
export default {
  components: {
    DefaultComp,
  },
  data() {
    return {
      allComponents: allComponents,
    };
  },
  methods: {
    addComp(e) {
      console.log(e);
      this.$emit('addComponent',e)
    },
  },
};
</script>
<style scoped lang='less'>
.left-view {
  width: 25%;
  background-color: #fbf2e3;
  height: 500px;
  .left-title {
    width: 100%;
    height: 30px;
    line-height: 30px;
    text-align: center;
  }
  .left-content {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
    justify-content: space-around;
  }
}
</style>