<template>
  <ul>
    <li v-for="link in links" :key="link.title">
      <slot name="link" :link="link" :handleMark="handleMark"></slot>
    </li>
  </ul>
</template>

<script>
export default {
  data () {
    return {
      links: [
        {
          href: 'https://www.pornhub.com',
          title: 'P',
          bookmarked: true
        },
        {
          href: 'https://www.xhmaster10.com',
          title: 'X',
          bookmarked: false
        }
      ]
    }
  },
  methods: {
    handleMark (link) {
      link.bookmarked = !link.bookmarked;
    }
  }
}
</script>

<style>

</style>
