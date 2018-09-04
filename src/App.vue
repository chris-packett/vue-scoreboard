<template>
  <div id="app">
    <Logo />
    <HelloWorld message="Welcome to the Vue Scoreboard!"/>
    <div class="teams">
      <Team teamName="Team 1" v-bind:teamScore="0" />
      <Team teamName="Team 2" v-bind:teamScore="0" />
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Logo from './components/Logo.vue'
import Team from './components/Team.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Logo,
    Team
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

.teams {
  display: flex;
  justify-content: space-evenly;
}
</style>
