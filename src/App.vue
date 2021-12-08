<template>
  <div class="container mx-auto">
    <map-static
      v-if="!isInteractive"
      :map="map"
      @setInteractive="setInteractive"
    ></map-static>
    <map-interactive v-else></map-interactive>
  </div>
</template>

<script>
import MapStatic from './components/MapStatic.vue'
import MapInteractive from './components/MapInteractive.vue'
import mapImg from './assets/static-map.png'
export default {
  name: 'App',
  components: {
    MapStatic,
    MapInteractive,
  },
  data() {
    return {
      map: mapImg,
      isInteractive: false,
    }
  },
  methods: {
    setInteractive() {
      this.isInteractive = true
    },
  },
}
</script>
