<template>
  <div id="app">
    <content></content>
  </div>
</template>

<script>
import Content from './components/Content.vue'

export default {
  name: 'app',
  components: {
    MenuBar
  }
}
</script>

<style scoped>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  height: 100%;
}
</style>
