<template>
    <div>
        <car-category @change="listenArt">
            <template v-slot:name>Fahrzeug</template>
            <car-tag-single :state="this.stateArt">Kleinwagen</car-tag-single>
            <car-tag-single :state="this.stateArt">Limousine</car-tag-single>
            <car-tag-single :state="this.stateArt">Kombi</car-tag-single>
        </car-category>
        <car-category @change="listenCraft">
            <template v-slot:name>Kraftstoffart</template>
            <car-tag-single :state="this.stateCraft">Diesel</car-tag-single>
            <car-tag-single :state="this.stateCraft">Benzin</car-tag-single>
            <car-tag-single :state="this.stateCraft">Elektro</car-tag-single>
        </car-category>
        <car-category>
            <template v-slot:name>Ausstattung</template>
            <car-tag>Sitzheizung</car-tag>
            <car-tag>Regemsensor</car-tag>
            <car-tag>Schibedach</car-tag>
            <car-tag>Tempomat</car-tag>
            <car-tag>Standheizung</car-tag>
        </car-category>
    </div>
</template>

<script>
import CarCategory from './_CarCategory'
import CarTag from './_CarTag'
import CarTagSingle from './_CarTagSingle'

export default {
  data () {
    return {
      stateArt: null,
      stateCraft: null
    }
  },
  components: {
    CarCategory,
    CarTag,
    CarTagSingle
  },
  methods: {
    listenArt: function (payload) {
      this.stateArt = payload
    },
    listenCraft: function (payload) {
      this.stateCraft = payload
    }
  }
}
</script>
