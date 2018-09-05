<template>
  <div id="app">
    <Logo />
    <HelloWorld message="Welcome to the Vue Scoreboard!"/>
    <Scoreboard />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Logo from './components/Logo.vue'
import Scoreboard from './components/Scoreboard.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Logo,
    Scoreboard
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
  margin-top: 2em;
}
</style>
