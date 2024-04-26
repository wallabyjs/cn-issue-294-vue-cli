<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <ChromePreview />
</template>

<script>
import ChromePreview from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    ChromePreview
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
