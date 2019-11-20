<template>
  <div id="app">
    <div id="menu">
      <ul>
        <li v-on:click="selectTab('Home')"><a>Home</a></li>
        <li v-on:click="selectTab('Work')"><a>Work</a></li>
        <li v-on:click="selectTab('Contact')"><a>Contact</a></li>
      </ul>
    </div>
    <pages :selection="selection"></pages>
  </div>
</template>

<script>
  import Pages from './components/Pages.vue'

  export default {
    name: 'app',
    data() {
      return {
        selection: 'Home',
      }
    },
    components: {
      Pages
    },
    methods: {
      selectTab(string) {
        this.selection = string;
      }
    }
  }
</script>

<style scoped>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    min-height: 100%;
  }
  #menu, ul {
    display: flex;
  }
  #menu {
    justify-content: center;
  }
  ul {
    justify-content: space-around;
  }
</style>
