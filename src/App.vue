<template>
  <LMap style="height: 100vh; width: 100vw" :zoom="13" :center="[50.45, 30.52]">
    <LTileLayer
      url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
      attribution="&copy; OpenStreetMap contributors"
    />
    <LMarker :lat-lng="[50.45, 30.52]">
      <LPopup>Київ 💙💛</LPopup>
    </LMarker>
  </LMap>
</template>

<script setup lang="ts">
import 'leaflet/dist/leaflet.css'
import { LMap, LTileLayer, LMarker, LPopup } from '@vue-leaflet/vue-leaflet'
import L from 'leaflet'
import iconUrl from 'leaflet/dist/images/marker-icon.png'
import iconRetinaUrl from 'leaflet/dist/images/marker-icon-2x.png'
import shadowUrl from 'leaflet/dist/images/marker-shadow.png'

// Fix for default marker icons when using Vite/ESM
L.Icon.Default.mergeOptions({
  iconRetinaUrl,
  iconUrl,
  shadowUrl
})
</script>

<style>
html, body, #app { margin: 0; height: 100%; }
</style>
