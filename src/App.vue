<template>
  <h1>{{ title }}</h1>
  <AppModal />
  <input type="text" ref="name">
  <button @click="handleClick">Click me</button>
</template>

<script>

import AppModal from './components/AppModal.vue'

export default {
  name: 'App',
  components: { AppModal },
  data() {
    return {
      title : 'my first vue app :)'
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

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
