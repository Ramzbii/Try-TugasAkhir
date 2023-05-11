<template>
    <div class="map" ref="map"></div>
</template>

<script setup>
const map = ref(null)
const { data : datas } = await useFetch('http://localhost/api/radar-location')
  

onMounted(() => {

  const mapDiv = L.map(map.value, {
    attributionControl: false,
    // zoomAnimation:false,
    zoomControl: false
  }).setView([ -6.484708, 106.837975], 10)

  const backgroundLayer = L.tileLayer(
    'https://tile.openstreetmap.org/{z}/{x}/{y}.png',
    {
      maxZoom: 18,
      minZoom: 5,
      id: 'mapbox/streets-v11'
    }
  )
  mapDiv.addLayer(backgroundLayer)
  mapDiv.setMaxBounds([[8, 93], [-13.2, 143.8]])


//overlay gambar
let imageUrl = 'https://www.linkpicture.com/q/cl_20210101_000010.png';
let errorOverlayUrl = 'https://cdn-icons-png.flaticon.com/512/110/110686.png';
let altText = 'Image of Newark, N.J. in 1922. Source: The University of Texas at Austin, UT Libraries Map Collection.';
let latLngBounds = L.latLngBounds([[ -6.134251, 106.673524], [-6.646620, 106.981601]]);
let imageOverlay = L.imageOverlay(imageUrl, latLngBounds, {
    opacity: 0.5,
    errorOverlayUrl: errorOverlayUrl,
    alt: altText,
    interactive: true
}).addTo(mapDiv);


  

  //membuat bulatan pada gsmap
datas.value.map(data => {
  console.log(data)
  let circle = L.circle([ data.radar_lat, data.radar_lon], {
    color: 'red',
    fillOpacity: 0.5,
    radius: 5
}).addTo(mapDiv);
  let radiusradar = L.circle([data.radar_lat, data.radar_lon], {
    color: 'grey',
    fillOpacity: 0.5,
    radius: 45000
}).addTo(mapDiv);
})
  
let circle_jakarta = L.circle([ -6.484616, 106.837954], {
    color: 'red',
    fillOpacity: 0.5,
    radius: 5
}).addTo(mapDiv);
  let radiusradar_jakarta = L.circle([-6.484616, 106.837954], {
    color: 'grey',
    fillOpacity: 0.5,
    radius: 45000
}).addTo(mapDiv);

})

</script>

<style>
.map {
  flex-grow: 1;
  background-color: #f5f6f4;
  z-index: 10;
}

</style>