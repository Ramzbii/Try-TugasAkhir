<template>
    <div class="map" ref="map"></div>
  </template>
  
  <script setup>
  const map = ref(null)
  
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
  
  })
  
  </script>
  
  <style>
  *,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  font-size: 62.5%;
  scroll-behavior: smooth;
}

body {
  font-family: 'Rubik', sans-serif;
  line-height: 1;
  font-size: 1.4rem;
  font-weight: 400;
  color: #2a2b26;
  min-width: 350px;
  overflow-x: hidden;
  background-color: #FCFAF9;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.noselect {
  -webkit-touch-callout: none;
  /* iOS Safari */
  -webkit-user-select: none;
  /* Safari */
  -khtml-user-select: none;
  /* Konqueror HTML */
  -moz-user-select: none;
  /* Old versions of Firefox */
  -ms-user-select: none;
  /* Internet Explorer/Edge */
  user-select: none;
  /* Non-prefixed version, currently supported by Chrome, Edge, Opera and Firefox */
}

/* Scrollbar */
::-webkit-scrollbar {
  width: 4px;
}

/* Track */
::-webkit-scrollbar-track {
  -webkit-box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
  -webkit-border-radius: 3px;
  border-radius: 2px;
}

/* Handle */
::-webkit-scrollbar-thumb {
  -webkit-border-radius: 3px;
  border-radius: 2px;
  background: rgba(225, 244, 203, 0.8);
  -webkit-box-shadow: inset 0 0 4px rgba(0, 0, 0, 0.5);
}

::-webkit-scrollbar-thumb:window-inactive {
  background: rgba(225, 244, 203, 0.4);
}

#__nuxt {
  display: flex;
  position: relative;
  flex-direction: column;
  min-height: 100vh;
  /* overflow: hidden; */
}
  .map {
    flex-grow: 1;
    background-color: #f5f6f4;
    z-index: 10;
  }
  </style>