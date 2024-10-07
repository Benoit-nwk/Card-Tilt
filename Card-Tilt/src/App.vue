<script setup>

let numberOfTheImage = 0
let urlOfImage = ``

let tabOfImages = []

const getNumber = () => {
    while(numberOfTheImage<=2){
      numberOfTheImage++
      urlOfImage = `https://picsum.photos/200/300?random=${numberOfTheImage}`
      tabOfImages.push(urlOfImage);
      
    }
}
console.log(tabOfImages);
getNumber()
</script>

<template>
  <div class="tab-of-card">
<div v-for="image in tabOfImages">
  <img :src="image" alt="randomImage">
</div>
</div>
</template>

<style scoped>
.tab-of-card{
  height: 100dvh;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 5rem;
}

img{
  border-radius: 1rem;
}
</style>
