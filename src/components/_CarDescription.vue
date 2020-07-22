<template>
    <div class="car-description">
        <div class="car-description__title">
            <slot name="title"></slot>
            <div @click="toggle" class="arrow" :class="{ 'arrow--open': show}">
              <svg xmlns="http://www.w3.org/2000/svg" width="12" height="7">
                <path fill="none" stroke="#666" stroke-width="1.5" d="M11 1L5.9 6 1 1"/>
              </svg>
            </div>
        </div>
        <div class="car-description__text" v-show="show">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      show: true
    }
  },

  methods: {
    toggle () {
      this.show = !this.show
    }
  }
}
</script>
