
<template>
  <div>
    <h1>PageOne</h1>
      <div class="container-1">
       <FeuFull />
      </div>
  </div>
</template>



<script>
import FeuFull  from '@/components/FeuFull.vue'


export default {
   name: 'PageOne',
   components: {
    FeuFull,
   }
}
</script>


<style scoped>

.html, body {
  padding: 0;
  margin: 0;
}

.container-1 {
  position: absolute;
  display: flex;
  border: 2px solid black;
  height: 100vh;
  width: 100vw;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  top: 0;
}


</style>
