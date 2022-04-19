<script setup lang="ts">
import entities from '../assets/entities.json'
import "leaflet/dist/leaflet.css"
import { LMap, LGeoJson, LTileLayer } from "@vue-leaflet/vue-leaflet";
</script>

<template>
    <l-map style="height:70vh" :center="center" :zoom="zoom"> 
    <l-tile-layer :url="url" :zoom="zoom" :attribution="attribution" />
    <l-geo-json :geojson="geojson" :options="geojsonOptions" />
    
    
  </l-map>
</template>


<script lang="ts">

export default {
  components: {
    LMap,
    LGeoJson,
    LTileLayer
  },
  data() {
    return {
      url: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      attribution:
        '&copy; <a target="_blank" href="http://osm.org/copyright">OpenStreetMap</a> contributors',
      zoom: 1,
      center: [48, -1.219482],
      geojson: entities,
      geojsonOptions: {
        // Options that don't rely on Leaflet methods.
      },
    };
  },

  async beforeMount() {
    function getColor(x) {
      if (x == "wholesaler"){
          return '#a83632'
      }
      else if (x == "retailer") {
          return '#2a2a2e'
      }
      else if (x == "import_port") {
          return '#ed00dd'
      }
      else if (x == "transit_port") {
          return '#00d9ed'
      }
      else if (x == "export_port") {
          return '#161716'
      }
      else if (x == "supplier") {
          return '#00ed0c'
      }
      else if (x == "manufacturer") {
          return '#f78000'
      }
  }
    //
    // HERE is where to load Leaflet components!
    // const { circleMarker } = await import("leaflet/dist/leaflet-src.esm");
    const { LMarker } = await import("leaflet/dist/leaflet-src.esm");
    const { circleMarker } = await import("leaflet/dist/leaflet-src.esm");
    // And now the Leaflet circleMarker function can be used by the options:
    // this.geojsonOptions.onEachFeature = (feature, layer) => 
    //     layer.bindPopup(feature.properties.entity_type + " " + feature.properties.id);
    this.geojsonOptions.onEachFeature = (feature, layer) => {
        layer.bindTooltip(feature.properties.entity_type + " " + feature.properties.id);
    }

    this.geojsonOptions.pointToLayer = (feature, latLng) => 
        circleMarker(latLng, {radius: 8, color: getColor(feature.properties.entity_type)})
    
    
    this.mapIsReady = true;
  },
};
</script>



<style scoped>

</style>