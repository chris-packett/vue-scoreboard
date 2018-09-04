<template>
  <div class="team">
    <Scoreboard v-bind:teamName="this.teamName" v-bind:teamScore="this.teamScore" />
    <Update />
  </div>
</template>

<script>
import Scoreboard from './Scoreboard.vue'
import Update from './Update.vue'

export default {
  name: "Team",
  components: {
    Scoreboard,
    Update
  },
  props: {
    teamName: String,
    teamScore: Number
  }
}
</script>

<style scoped>
.team-score {
  font-size: 48px;
}
</style>
