<template>
    <div class="car-tag" @click="select" :class="{ 'car-tag--selected': clicked}">
        <slot></slot>
    </div>
</template>

<script>
export default {
  data () {
    return {
      clicked: false
    }
  },
  methods: {
    select () {
      this.clicked = !this.clicked
      this.$parent.$emit('change', true)
    }
  }
}
</script>
