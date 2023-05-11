<template>
  <!-- <TheHeader></TheHeader>
    <TheButtons></TheButtons> -->
    <NuxtPage></NuxtPage>
  <!-- <TheMap></TheMap> -->
</template>



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
</style>