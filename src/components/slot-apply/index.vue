<template>
  <div>
    <ActionBar>
      <component :is="slotContent"/>
    </ActionBar>
    <WebApp @slot-content="component => slotContent = component"/>
  </div>
</template>

<script>
// 1.向下使用 props，向上使用 event
import ActionBar from './action-bar';
import WebApp from './web-app';

export default {
  data () {
    return {
      slotContent: ''
    }
  },
  components: {
    ActionBar,
    WebApp
  }
}
</script>

<style>

</style>
