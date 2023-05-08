<script setup>
definePageMeta({
  layout: "custom",
});

const setLayoutToDefault = ()=>{
    setPageLayout('default')
}
const setLayoutToCustom = ()=>{
    setPageLayout('custom')
}
</script>   
<template>
    <div>
        <div>PAGE Contact</div>
        <div class="flex space-x-4">
        <button @click="setLayoutToDefault" >Kembalikan ke default</button>
        <button @click="setLayoutToCustom" >Kembalikan ke custom</button>
        </div>
    </div>
</template>