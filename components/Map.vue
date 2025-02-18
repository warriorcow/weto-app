<script setup lang="ts">
import { onMounted } from 'vue'
import maplibregl from 'maplibre-gl'
import 'maplibre-gl/dist/maplibre-gl.css'

onMounted(() => {
  const map = new maplibregl.Map({
    container: 'map', // ID контейнера
    style: 'https://api.maptiler.com/maps/streets-v2/style.json?key=eLa6g9Y2oCa8h1cPpsJF',
    center: [37.618423, 55.751244], // Москва (долгота, широта)
    zoom: 10
  })

  // Добавляем управление масштабированием
  map.addControl(new maplibregl.NavigationControl())

  // Добавляем метку
  new maplibregl.Marker()
      .setLngLat([37.618423, 55.751244]) // Координаты
      .setPopup(new maplibregl.Popup().setText('Привет, Москва!')) // Попап при клике
      .addTo(map)
})
</script>

<template>
  <div id="map" class="map-container"></div>
</template>

<style scoped>
.map-container {
  width: 100%;
  height: 90vh;
}
</style>
