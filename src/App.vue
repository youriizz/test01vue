<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name">
  <button @click="handleClick">Click me</button>
  <div class="container-1">
    <div class="redcircle-container">
        <RedCircle :CircleText="CircleText"/>
    </div>
  </div>

</template>

<script>

import RedCircle from './components/redcircle.vue'

export default {
  name: 'App',
  components: { 
    RedCircle,           
   },
  data() {
    return {
      title : 'my first vue app :)',
      CircleText: 'wesh bien ou quoi'
    }
  }, 
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
    }
  }
}
</script>

<style>

.html, body {
  padding: 0;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  padding: 0;
}

.container-1 {
  position: absolute;
  display: flex;
  border: 2px solid black;
  height: 100vh;
  width: 100vw;
  align-items: center;
  justify-content: center;
  top: 0;
  box-sizing: border-box;
}

.redcircle-container {
  position: absolute;
}
</style>
