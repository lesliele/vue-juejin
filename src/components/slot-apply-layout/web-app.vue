<template>
  <Layout>
    <template #actionbar>
      <SlotContent/>
    </template>
    <p>This is main content</p>
  </Layout>
</template>

<script>
import Layout from './layout';
import SlotContent from './slot-content';

export default {
  components: {
    Layout,
    SlotContent
  }
}
</script>

<style>

</style>
