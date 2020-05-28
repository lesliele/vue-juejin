<script>
export default {
  props: ['value'],
  data () {
    return {
      newTag: ''
    }
  },
  methods: {
    addTag() {
      this.$emit('input', [...this.value, this.newTag.trim()])
      this.newTag = '';
    },
    removeTag(tag) {
      this.$emit('input', this.value.filter(t => t !== tag));
    }
  },
  render () {
    return this.$scopedSlots.default({
      tagsSlot: this.value,
      removeTag: this.removeTag,
      inputAttrs: {
        value: this.newTag
      },
      inputEvents: {
        input: (e) => {this.newTag = e.target.value},
        keydown: (e) => {
          if (e.keyCode === 13) {
            e.preventDefault();
            this.addTag();
          }
        }
      }
    })
  }
}
</script>
