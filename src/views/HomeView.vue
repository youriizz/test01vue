<template>
  <div>
    <h1>HomeView</h1>
  <div class="container-red">
    <RouterLink to="/page-one">
      <RedCircle :targetRoute="'/page-one'" />
    </RouterLink>
  </div>
</div>
</template>


<script>

import RedCircle from '@/components/FeuRouge.vue'

export default {
  name: 'HomeView',
  components: { 
    RedCircle,          
   }
  }

</script>

<style scoped>

.html, body {
  padding: 0;
  margin: 0;
}


.container-red {
  position: absolute;
  display: flex;
  border: 2px solid rgb(40, 31, 31);
  height: 20vh;
  width: 20vw;
  align-items: center;
  justify-content: center;
  top: 0;
  box-sizing: border-box;
}

</style>
