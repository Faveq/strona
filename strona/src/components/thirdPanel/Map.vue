<script setup lang="ts">
import { onMounted, ref } from "vue";
import L, { LatLng, Marker, Map } from "leaflet";

const lat = ref<number>(0);
const lng = ref<number>(0);
const map = ref<Map>();
const mapContainer = ref<HTMLDivElement>();

onMounted(() => {
  if (mapContainer.value) {
    map.value = L.map(mapContainer.value).setView([51.505, -0.09], 13);
    L.tileLayer("https://tile.openstreetmap.org/{z}/{x}/{y}.png", {
      maxZoom: 19,
      attribution:
        '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
    }).addTo(map.value);
  }
});

function getLocation() {
  if (navigator.geolocation) {
    navigator.geolocation.watchPosition((position) => {
      lat.value = position.coords.latitude;
      lng.value = position.coords.longitude;
      if (map.value) {
        map.value.setView([lat.value, lng.value], 13);
      }
    });
  }
}
</script>

<template>
  <button @click="getLocation()">Get Location</button>
  {{ lat }} , {{ lng }}

  <div ref="mapContainer" style="width: 400px; height: 400px"></div>
</template>

<style scoped>
</style>