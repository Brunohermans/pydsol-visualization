<script setup lang="ts">
import "leaflet/dist/leaflet.css"
import { LMap, LGeoJson, LTileLayer } from "@vue-leaflet/vue-leaflet";
</script>

<template>
    <l-map style="height:70vh" :center="center"> 
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
      geojson: {
        type: "FeatureCollection",
        features: [
          { "type": "Feature", "properties": { "id": "0", "entity_type": "supplier" }, "geometry": { "type": "Point", "coordinates": [ 105.730582874588222, 10.209046981023137 ] } },
{ "type": "Feature", "properties": { "id": "1", "entity_type": "supplier" }, "geometry": { "type": "Point", "coordinates": [ 105.736415675114543, 18.731267101728296 ] } },
{ "type": "Feature", "properties": { "id": "2", "entity_type": "supplier" }, "geometry": { "type": "Point", "coordinates": [ 106.312575322718757, 10.120914131543831 ] } },
{ "type": "Feature", "properties": { "id": "3", "entity_type": "manufacturer" }, "geometry": { "type": "Point", "coordinates": [ 105.659262538389655, 19.72813157273637 ] } },
{ "type": "Feature", "properties": { "id": "4", "entity_type": "manufacturer" }, "geometry": { "type": "Point", "coordinates": [ 106.101407186446863, 10.410772488682802 ] } },
{ "type": "Feature", "properties": { "id": "5", "entity_type": "manufacturer" }, "geometry": { "type": "Point", "coordinates": [ 105.039992562968791, 18.95372602601125 ] } },
{ "type": "Feature", "properties": { "id": "6", "entity_type": "manufacturer" }, "geometry": { "type": "Point", "coordinates": [ 105.650327975517499, 9.742940218647437 ] } },
{ "type": "Feature", "properties": { "id": "7", "entity_type": "manufacturer" }, "geometry": { "type": "Point", "coordinates": [ 105.498918598807151, 18.719265340709832 ] } },
{ "type": "Feature", "properties": { "id": "8", "entity_type": "export_port" }, "geometry": { "type": "Point", "coordinates": [ 105.825000203000059, 19.316773351000052 ] } },
{ "type": "Feature", "properties": { "id": "9", "entity_type": "export_port" }, "geometry": { "type": "Point", "coordinates": [ 106.208716940000045, 9.543922678000058 ] } },
{ "type": "Feature", "properties": { "id": "10", "entity_type": "transit_port" }, "geometry": { "type": "Point", "coordinates": [ 106.912098768000078, 20.966640614000084 ] } },
{ "type": "Feature", "properties": { "id": "11", "entity_type": "import_port" }, "geometry": { "type": "Point", "coordinates": [ 3.59053, 51.44503 ] } },
{ "type": "Feature", "properties": { "id": "12", "entity_type": "wholesaler" }, "geometry": { "type": "Point", "coordinates": [ 4.105660195136984, 51.907968374694875 ] } },
{ "type": "Feature", "properties": { "id": "13", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.15782549686376, 51.890456372321061 ] } },
{ "type": "Feature", "properties": { "id": "14", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.538324425907971, 51.865104388704623 ] } },
{ "type": "Feature", "properties": { "id": "15", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.651382148895649, 51.583044779199795 ] } },
{ "type": "Feature", "properties": { "id": "16", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.651996548733654, 52.514628138332341 ] } },
{ "type": "Feature", "properties": { "id": "17", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.849365963451653, 52.381167315487566 ] } },
{ "type": "Feature", "properties": { "id": "18", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.33364301030617, 51.683267320716247 ] } },
{ "type": "Feature", "properties": { "id": "19", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.778410142894169, 52.952214093594414 ] } },
{ "type": "Feature", "properties": { "id": "20", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.104630747450149, 52.190599619805489 ] } },
{ "type": "Feature", "properties": { "id": "21", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 4.299222895121797, 52.073364879395484 ] } },
{ "type": "Feature", "properties": { "id": "22", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.049048212814635, 52.107201248727527 ] } },
{ "type": "Feature", "properties": { "id": "23", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.676510360182933, 51.907901161056685 ] } },
{ "type": "Feature", "properties": { "id": "24", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 3.913651680323567, 51.653707896507555 ] } },
{ "type": "Feature", "properties": { "id": "25", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.520248537758084, 51.610394912799826 ] } },
{ "type": "Feature", "properties": { "id": "26", "entity_type": "retailer" }, "geometry": { "type": "Point", "coordinates": [ 5.640281089580302, 52.044512983633901 ] } },
{ "type": "Feature", "properties": { "id": "(0, 3)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.730582874588222, 10.209046981023137 ], [ 105.659262538389655, 19.72813157273637 ] ] } },
{ "type": "Feature", "properties": { "id": "(0, 6)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.730582874588222, 10.209046981023137 ], [ 105.650327975517499, 9.742940218647437 ] ] } },
{ "type": "Feature", "properties": { "id": "(1, 5)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.736415675114543, 18.731267101728296 ], [ 105.039992562968791, 18.95372602601125 ] ] } },
{ "type": "Feature", "properties": { "id": "(1, 7)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.736415675114543, 18.731267101728296 ], [ 105.498918598807151, 18.719265340709832 ] ] } },
{ "type": "Feature", "properties": { "id": "(2, 4)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.312575322718757, 10.120914131543831 ], [ 106.101407186446863, 10.410772488682802 ] ] } },
{ "type": "Feature", "properties": { "id": "(2, 6)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.312575322718757, 10.120914131543831 ], [ 105.650327975517499, 9.742940218647437 ] ] } },
{ "type": "Feature", "properties": { "id": "(3, 8)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.659262538389655, 19.72813157273637 ], [ 105.825000203000059, 19.316773351000052 ] ] } },
{ "type": "Feature", "properties": { "id": "(4, 8)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.101407186446863, 10.410772488682802 ], [ 105.825000203000059, 19.316773351000052 ] ] } },
{ "type": "Feature", "properties": { "id": "(4, 9)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.101407186446863, 10.410772488682802 ], [ 106.208716940000045, 9.543922678000058 ] ] } },
{ "type": "Feature", "properties": { "id": "(5, 8)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.039992562968791, 18.95372602601125 ], [ 105.825000203000059, 19.316773351000052 ] ] } },
{ "type": "Feature", "properties": { "id": "(6, 8)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.650327975517499, 9.742940218647437 ], [ 105.825000203000059, 19.316773351000052 ] ] } },
{ "type": "Feature", "properties": { "id": "(6, 9)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.650327975517499, 9.742940218647437 ], [ 106.208716940000045, 9.543922678000058 ] ] } },
{ "type": "Feature", "properties": { "id": "(7, 8)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.498918598807151, 18.719265340709832 ], [ 105.825000203000059, 19.316773351000052 ] ] } },
{ "type": "Feature", "properties": { "id": "(8, 10)", "entity_type": "sealink" }, "geometry": { "type": "LineString", "coordinates": [ [ 105.825000203000059, 19.316773351000052 ], [ 106.912098768000078, 20.966640614000084 ] ] } },
{ "type": "Feature", "properties": { "id": "(9, 10)", "entity_type": "sealink" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.208716940000045, 9.543922678000058 ], [ 106.912098768000078, 20.966640614000084 ] ] } },
{ "type": "Feature", "properties": { "id": "(10, 11)", "entity_type": "sealink" }, "geometry": { "type": "LineString", "coordinates": [ [ 106.912098768000078, 20.966640614000084 ], [ 3.59053, 51.44503 ] ] } },
{ "type": "Feature", "properties": { "id": "(11, 12)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 3.59053, 51.44503 ], [ 4.105660195136984, 51.907968374694875 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 23)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.676510360182933, 51.907901161056685 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 13)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.15782549686376, 51.890456372321061 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 14)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.538324425907971, 51.865104388704623 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 15)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.651382148895649, 51.583044779199795 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 16)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.651996548733654, 52.514628138332341 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 17)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.849365963451653, 52.381167315487566 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 18)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.33364301030617, 51.683267320716247 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 19)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.778410142894169, 52.952214093594414 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 20)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.104630747450149, 52.190599619805489 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 21)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 4.299222895121797, 52.073364879395484 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 22)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.049048212814635, 52.107201248727527 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 24)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 3.913651680323567, 51.653707896507555 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 25)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.520248537758084, 51.610394912799826 ] ] } },
{ "type": "Feature", "properties": { "id": "(12, 26)", "entity_type": "link" }, "geometry": { "type": "LineString", "coordinates": [ [ 4.105660195136984, 51.907968374694875 ], [ 5.640281089580302, 52.044512983633901 ] ] } }
        ],
      },
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