<template>
  <div class="team-scoreboard-container">
    <h4 class="team-name">{{ teamName }}</h4>
    <h1 class="team-score">{{ teamScore }}</h1>
  </div>
</template>

<script>
export default {
  name: "Scoreboard",
  props: {
    teamName: String,
    teamScore: Number
  }
}
</script>

<style scoped>
</style>
