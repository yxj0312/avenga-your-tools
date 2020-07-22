<template>
    <div class="car-tag" @click="select" :class="{ 'car-tag--selected': check()}">
        <slot></slot>
    </div>
</template>

<script>
export default {
  props: ['state'],
  data () {
    return {
      clicked: false,
      selected: false
    }
  },
  methods: {
    select () {
      this.clicked = !this.clicked
      this.$parent.$emit('change', this.$el.innerHTML)
    },

    check () {
      if (this.$el !== undefined) {
        this.selected = (this.$el.innerHTML === this.state)
      }
      return (this.selected && ((this.$el !== undefined) ? this.$el.innerHTML === this.state : true))
    }
  }
}
</script>
