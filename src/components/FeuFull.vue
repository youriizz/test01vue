<template>

    <div class="container-red">
      <RedCircle :targetRoute="redRoute" />
    </div>
    <div class="container-orange">
      <OrangeCircle :targetRoute="orangeRoute" />
    </div>
    <div class="container-green">
      <GreenCircle :targetRoute="greenRoute" />

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
   props: {
    redRoute: String,
    orangeRoute: String,
    greenRoute: String
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
