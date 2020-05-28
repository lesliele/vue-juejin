<template>
  <div>
    <input-tag v-model="tags">
      <div slot-scope="{tagsSlot, removeTag, inputAttrs, inputEvents}" class="tags-input">
        <span class="tags-class-tag">
          <span v-for="tag in tagsSlot" :key="tag">
            <span>{{tag}}</span>
            <button type="button" class="tags-input-remove" @click="removeTag(tag)">del</button>
          </span>
        </span>
        <input class="tags-input-text" placeholder="add tags..." v-bind="inputAttrs" v-on="inputEvents"/>
      </div>
    </input-tag>
  </div>
</template>

<script>
import InputTag from './input-tag';

export default {
  data () {
    return {
      tags: ['Testing', 'Design']
    }
  },
  components: {
    InputTag
  }
}
</script>

<style>

</style>
