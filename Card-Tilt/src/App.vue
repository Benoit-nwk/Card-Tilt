<script setup>
import Reload from './components/Reload.vue';
let numberOfTheImage = 0


let tabOfImages = []

const getNumber = () => {
    while(numberOfTheImage<=2){
      numberOfTheImage++
      let urlOfImage = `https://picsum.photos/330/500?random=${numberOfTheImage}`
      tabOfImages.push(urlOfImage);
      
    }
}
console.log(tabOfImages);
getNumber()
</script>

<template>
  <h1>Card-Tilt</h1>
  <div class="tab-of-card">
<div v-for="image in tabOfImages">
  <img :src="image" alt="randomImage">
</div>
</div>
<Reload/>
</template>

<style scoped>


</style>
