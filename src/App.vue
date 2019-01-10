<template>
  <div id="app">
    <questions></questions>
  </div>
</template>

<script>
import Questions from './components/Questions'
export default {
  name: 'app',
  components: {
    Questions
  },
  data () {
    return {
      diesAndEnded: false
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
