<template>
    <div class="OrangeCircle" @click="navigate"></div>
</template>

<script>
export default {
  name: 'OrangesCircle',
  props: {
      targetRoute: {
          type: String,
          default: '/'
      }
  },
  methods: {
      navigate() {
          this.$router.push(this.targetRoute);
      }
  }
}
</script>

 <style scoped>

.OrangeCircle {
  position: relative;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: Orange;
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: pointer;
}

.OrangeCircle:active,
.OrangeCircle:hover,
.OrangeCircle:focus {
  transform: scale(1.2);
  box-shadow: 0 0 20px Orange;
  opacity: 100%;
  
}

@media (min-width: 600px) {
  .OrangeCircle {
    width: 80px;
    height: 80px;
  }
}

@media (max-width: 350px) {
 .OrangeCircle {
    width: 40px;
    height: 40px;
  }
}
</style>