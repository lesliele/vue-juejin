<template>
  <div class="main">
    <p>This is main content</p>
  </div>
</template>
<script>
import SlotContent from './slot-content.vue';

export default {
  created() {
    // As soon as this component is created we'll emit our events
    console.log('发起事件')
    this.$emit('slot-content', SlotContent);
  }
}
</script>

