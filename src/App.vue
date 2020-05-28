<template>
  <div id="app">
    <!-- <slotApply/> -->
    <!-- <slotApplyOptions/> -->
    <!-- <slotApplyLayout/> -->
    <!-- <slotScope/> -->
    <RenderLess/>
  </div>
</template>

<script>
// https://juejin.im/post/5e531139e51d452715155b62 (高级 Vue 技巧：控制父类的 slot)
// 1.向下使用 props，向上使用 event
// import slotApply from './components/slot-apply/index';
// 2.使用 $options
// import slotApplyOptions from './components/slot-apply-options/index';
// 3.提升状态
// import slotApplyLayout from './components/slot-apply-layout/index';
// 4.作用域插槽
// import slotScope from './components/slot-scope(作用域插槽)/index';
// 5.https://juejin.im/post/5c2d7030f265da613a54236f#comment 函数式组件运用(提供业务逻辑，并非官方说的函数式组件)
import RenderLess from './components/renderless/index';


export default {
  name: 'App',
  components: {
    // slotApply,
    // slotApplyOptions
    // slotApplyLayout
    // slotScope
    RenderLess
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
