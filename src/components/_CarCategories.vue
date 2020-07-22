<template>
    <div>
        <car-category>
            <template v-slot:name>Fahrzeug</template>
            <car-tag>Kleinwagen</car-tag>
            <car-tag>Limousine</car-tag>
            <car-tag>Kombi</car-tag>
        </car-category>
        <car-category>
            <template v-slot:name>Kraftstoffart</template>
            <car-tag>Diesel</car-tag>
            <car-tag>Benzin</car-tag>
            <car-tag>Elektro</car-tag>
        </car-category>
    </div>
</template>

<script>
import CarCategory from './_CarCategory'
import CarTag from './_CarTag'

export default {
  components: {
    CarCategory,
    CarTag
  }
}
</script>
