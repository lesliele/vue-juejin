<template>
  <LinkList>
    <div slot="link" slot-scope="{ link, handleMark}">
      <span>It's a greet website? {{link.bookmarked}}</span>
      <a :href="link.href">{{link.title}}</a>
      <button @click="handleMark(link)">权限控制 => 反向</button>
    </div>
  </LinkList>
</template>

<script>
import LinkList from './link-list';

export default {
  components: {
    LinkList
  }
}
</script>

<style>

</style>
