<template>

    <div class="container-red">
      <RedCircle />
    </div>
    <div class="container-orange">
      <OrangeCircle />
    </div>
    <div class="container-green">
      <GreenCircle />

  </div>

</template>

<script>

import RedCircle from '@/components/FeuRouge.vue'
import OrangeCircle from '@/components/FeuOrange.vue'
import GreenCircle from '@/components/FeuVert.vue'


export default {
  name: 'FeuFull',
  components: { 
    RedCircle, 
    OrangeCircle,
    GreenCircle        
   },
}
</script>

<style scoped>

.html, body {
  padding: 0;
  margin: 0;
}

.container-red {
  position: absolute;
  transform: translateY(-120%);
}


.container-orange {
  position: absolute;
  transform: translateY(0%);
}

.container-green {
  position: absolute;
  transform: translateY(120%);
}


</style>
