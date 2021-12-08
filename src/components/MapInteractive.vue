<template>
  <div ref="map" class="map"></div>
</template>

<script>
import Map from 'ol/Map'
import View from 'ol/View'
import OSM from 'ol/source/OSM'
import TileLayer from 'ol/layer/Tile'
import 'ol/ol.css'

export default {
  mounted() {
    new Map({
      layers: [new TileLayer({ source: new OSM() })],
      view: new View({
        center: [0, 0],
        zoom: 2,
      }),
      target: this.$refs.map,
    })
  },
}
</script>

<style scoped>
.map {
  height: 400px;
  width: 100%;
}
</style>
