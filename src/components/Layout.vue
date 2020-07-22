<template>
    <!-- Eigentlich ein Layout Komponent hier ist überflüssig, aber bei praktische Arbeit ist ein Layout 'good practice' -->
    <div class="layout">
        <layout-header></layout-header>
        <main>
          <car-categories></car-categories>
          <!-- <car-descriptions></car-descriptions> -->
        </main>
    </div>
</template>

<script>
import LayoutHeader from './_LayoutHeader.vue'
import CarCategories from './_CarCategories.vue'
// import CarDescriptions from './_CarDescriptions.vue'

export default {
  props: [],

  components: {
    LayoutHeader,
    CarCategories
    // CarDescriptions
  },

  computed: {

  },

  methods: {

  }
}
</script>
