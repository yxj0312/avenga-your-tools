<template>
    <div>
        <div>
            <slot name="title"></slot>
            <div @click="toggle">arrow</div>
        </div>
        <div v-show="show">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      show: false
    }
  },

  methods: {
    toggle () {
      this.show = !this.show
    }
  }
}
</script>
