<script setup>
import L from 'leaflet'
import 'leaflet/dist/leaflet.css'
import { onMounted } from 'vue'

onMounted(() => {
    const map = L.map('map').setView([51.505, -0.09], 13)
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 4,
        attribution: '© OpenStreetMap'
    }).addTo(map)

})


</script>

<template>
    <div>
        <div id="map"></div>
    </div>
</template>

<style lang="less" scoped>
#map {
    height: 100vh;
    width: 100vw;
}
</style>