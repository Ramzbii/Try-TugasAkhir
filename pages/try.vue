<template>
  <div>
    Counter: {{ counter }}
    <button @click="counter++">
      +
    </button>
    <button @click="counter--">
      -
    </button>

    <div v-for="p in products">
      <!-- <NuxtLink :to="`/api/dbz/${p.path}/${p.filename}`">API</NuxtLink> -->
      {{ p.products }}
    </div>
  </div>
</template>



<script setup>
const counter = useState('counter', () => Math.round(Math.random() * 1000))

 const { data : products }=await useFetch('http://localhost/api/radar-location')
 products.value.map(data => {
  console.log(data)
 })
//  console.log(products.value[0])
</script>

