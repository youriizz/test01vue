<template>
  <div class="RedCircle" @click="navigate"></div>
</template>

<script>
export default {
  name: 'RedCircle',
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

.RedCircle {
  position: relative;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: red;
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: pointer;
}

.RedCircle:active,
.RedCircle:hover,
.RedCircle:focus {
  transform: scale(1.2);
  box-shadow: 0 0 20px red;
  opacity: 100%;
  
}

@media (min-width: 600px) {
  .RedCircle {
    width: 80px;
    height: 80px;
  }
}

@media (max-width: 350px) {
 .RedCircle {
    width: 40px;
    height: 40px;
  }
}
</style>