<template>
  <div>
    <ActionBar>
      <slot name="actionbar"></slot>
    </ActionBar>
    <slot />
  </div>
</template>

<script>
import ActionBar from './action-bar';

export default {
  components: {
    ActionBar
  }
}
</script>

<style>

</style>
