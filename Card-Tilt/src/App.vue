<script setup>
import { onMounted, ref } from 'vue';
import Reload from './components/Reload.vue';
import VanillaTilt from 'vanilla-tilt';

const element=ref(null);
onMounted(()=>{
  VanillaTilt.init(element.value, { max: 10, speed:400 })
})

let numberOfTheImage = 0;
let tabOfImages = [];

const getNumber = () => {
    while(numberOfTheImage<=2){
      numberOfTheImage++;
      let urlOfImage = `https://picsum.photos/330/500?random=${numberOfTheImage}`;
      tabOfImages.push(urlOfImage);
    }
}

getNumber()

</script>

<template>
<h1>Card-Tilt</h1>
  <div class="tab-of-card">
    <div v-for="image in tabOfImages" class="card" ref="element">
        <img :src="image" alt="randomImage" width="330" height="500">
  </div>
</div>
<Reload/>
</template>

<style scoped>
.card{
  width: max-content;
  transform: perspective(1000px)
}

</style>
