<template>
  <div id="app">
    <Logo />
    <HelloWorld message="Welcome to the Vue Scoreboard!"/>
    <div class="teams">
      <div class="team">
        <Scoreboard v-bind:teamName="teamOneName" v-bind:teamScore="teamOneScore" />
        <Update />
      </div>
      <div class="team">
        <Scoreboard v-bind:teamName="teamTwoName" v-bind:teamScore="teamTwoScore" />
        <Update />
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Logo from './components/Logo.vue'
import Scoreboard from './components/Scoreboard.vue'
import Update from './components/Update.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Logo,
    Scoreboard,
    Update
  },
  data: function () {
    return {
      teamOneName: 'Team 1 Name',
      teamOneScore: 0,
      teamTwoName: 'Team 2 Name',
      teamTwoScore: 0
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
  margin-top: 2em;
}

.teams {
  display: flex;
  justify-content: space-evenly;
}

.team-score {
  font-size: 48px;
}
</style>
