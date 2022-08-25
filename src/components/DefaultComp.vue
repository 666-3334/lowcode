<script>
// 默认组件效果
import allComponents from "./getAllComps";
export default {
  data() {
    return {};
  },
  props: {
    compIndex: {
      type: Number,
      default: 0,
    },
  },
  computed: {
    // finalStyle() {
    //   return {
    //     width: allComponents[this.compIndex].attributes[0].value + "px",
    //   };
    // },
  },
  methods: {
    dragStart(e) {
      console.log(e.target.dataset.compindex); //string
    },
    dragend(e) {
      let screenWidth = document.documentElement.clientWidth;
      if (e.screenX > screenWidth * 0.25 && e.screenX < screenWidth * 0.75) {
        this.$emit("addComp", e.target.dataset.compindex);
      }
    },
  },
  render() {
    return (
      <div
        class="default-item"
        draggable="true"
        data-compindex={this.compIndex}
        onDragstart={this.dragStart}
        onDragend={this.dragend}
      >
        {allComponents[this.compIndex].compName}
      </div>
    );
  },
};
</script>
<style scoped lang='less'>
.default-item {
  width: 40%;
  height: 100px;
  margin-bottom: 10px;
  background-color: #fff;
}
</style>