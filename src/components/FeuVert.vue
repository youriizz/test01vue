<template>
    <div class="GreenCircle" @click="navigate"></div>
</template>

<script>
export default {
  name: 'GreenCircle',
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

.GreenCircle {
  position: relative;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: Green;
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: pointer;
}

.GreenCircle:active,
.GreenCircle:hover,
.GreenCircle:focus {
  transform: scale(1.2);
  box-shadow: 0 0 20px Green;
  opacity: 100%;
  
}

@media (min-width: 600px) {
  .GreenCircle {
    width: 80px;
    height: 80px;
  }
}

@media (max-width: 350px) {
 .GreenCircle {
    width: 40px;
    height: 40px;
  }
}
</style>