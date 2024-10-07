<script setup>

const reloadPage = () =>{
      window.location.reload();
}


</script>

<template>
<div>
      <button @click="reloadPage">Reload images</button>
</div>
</template>

<style scoped>
button{
      background: none;
      color: aliceblue;
      border: 0.2rem solid white;
      border-radius: 2rem;
      padding: 1rem;
      font-size: large;
      transition: all 0.5s ease;
}

button:hover{
      scale: 1.1;
      background-color: aliceblue;
      color: black;
      cursor: pointer;
}

div{
      margin-top: 2rem;
      display: flex;
      justify-content: center;
      align-items: center;
}
</style>