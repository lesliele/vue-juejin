<template>
  <div id="app">
    <!-- <slotApply/> -->
    <!-- <slotApplyOptions/> -->
    <slotApplyLayout/>
  </div>
</template>

<script>
// https://juejin.im/post/5e531139e51d452715155b62 (高级 Vue 技巧：控制父类的 slot)
// 1.向下使用 props，向上使用 event
// import slotApply from './components/slot-apply/index';
// 2.使用 $options
// import slotApplyOptions from './components/slot-apply-options/index';
// 3.提升状态
import slotApplyLayout from './components/slot-apply-layout/index';

export default {
  name: 'App',
  components: {
    // slotApply,
    // slotApplyOptions
    slotApplyLayout
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
