<template>
  <div class="top-view">{{ msg }}</div>
</template>

<script>
export default {
  data() {
    return {
      msg: "LowCode,making life better!",
    };
  },
};
</script>
<style scoped lang='less'>
.top-view {
  margin: 0 auto 10px;
  width: 88%;
  height: 40px;
  line-height: 40px;
  font-size: 20px;
  box-sizing: border-box;
  padding:0 2%;
  border-bottom: 1px solid #d6d7d7;
}
</style>