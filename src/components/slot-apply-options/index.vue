<template>
  <div>
    <ActionBar>
      <component :is="slotContent"/>
    </ActionBar>
    <WebApp/>
  </div>
</template>

<script>
// 2.使用 $options
import ActionBar from './action-bar';
import WebApp from './web-app';

export default {
  data () {
    return {
      slotContent: WebApp.slotContent
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
