<script>
// 实际组件效果
import allComponents from "./getAllComps";
export default {
  props: {
    compIndex: {
      type: Number,
      default: 0,
    },
    // fianlStyle: {
    //   type: Object,
    // },
    // finalData: {
    //   type: String,
    // },
  },
  methods:{
    clickComp(e){
        console.log(e);
        this.$emit('clickComp',e)
    }
  },
  render() {
    // if (allComponents[this.compIndex].compType == "span")
      return (
        <div onClick={this.clickComp}>
          <span>{allComponents[this.compIndex].cdata}</span>
        </div>
      );
  },
};
</script>
<style scoped lang='less'>
</style>