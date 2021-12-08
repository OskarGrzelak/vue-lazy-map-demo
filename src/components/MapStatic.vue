<template>
  <img
    :src="map"
    alt="Static map"
    class="map"
    @click="$emit('set-interactive')"
  />
</template>

<script>
export default {
  props: ['map'],
  emits: ['set-interactive'],
}
</script>

<style scoped>
.map {
  width: 100%;
}
</style>
