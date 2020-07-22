<template>
    <!-- Eigentlich ein Layout Komponent hier ist überflüssig, aber bei praktische Arbeit ist ein Layout 'good practice' -->
    <div class="layout">
        <layout-header></layout-header>
        <main>
        </main>
    </div>
</template>

<script>
import LayoutHeader from './_LayoutHeader.vue'

export default {
  props: [],

  components: {
    LayoutHeader
  },

  computed: {

  },

  methods: {

  }
}
</script>
