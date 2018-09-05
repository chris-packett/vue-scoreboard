<template>
  <div class="teams">
    <div class="team">
      <div class="team-scoreboard-container">
        <h4 class="team-name">{{ teamOneName }}</h4>
        <h1 class="team-score">{{ teamOneScore }}</h1>
      </div>
      <div class="team-update-container">
        <div class="team-update-name">
          <h4>Update Team Name:</h4>
          <div class="team-update-name-input-and-button">
            <input type="text" placeholder="Update team name..." v-model='teamOneNameInput'>
            <button v-on:click='updateTeamOneName'>Update</button>
          </div>
        </div>
        <div class="team-update-score">
          <h4>Update Team Score:</h4>
          <div class="team-update-score-buttons">
            <button v-on:click='addOneToTeamOneScore'>Add 1</button>
            <button v-on:click='subOneFromTeamOneScore'>Subtract 1</button>
          </div>
        </div>
      </div>
    </div>
    <div class="team">
      <div class="team-scoreboard-container">
        <h4 class="team-name">{{ teamTwoName }}</h4>
        <h1 class="team-score">{{ teamTwoScore }}</h1>
      </div>
      <div class="team-update-container">
        <div class="team-update-name">
          <h4>Update Team Name:</h4>
          <div class="team-update-name-input-and-button">
            <input type="text" placeholder="Update team name..." v-model='teamTwoNameInput'>
            <button v-on:click='updateTeamTwoName'>Update</button>
          </div>
        </div>
        <div class="team-update-score">
          <h4>Update Team Score:</h4>
          <div class="team-update-score-buttons">
            <button v-on:click='addOneToTeamTwoScore'>Add 1</button>
            <button v-on:click='subOneFromTeamTwoScore'>Subtract 1</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Scoreboard",
  data: function () {
    return {
      teamOneName: 'Team 1 Name',
      teamOneNameInput: '',
      teamOneScore: 0,
      teamTwoName: 'Team 2 Name',
      teamTwoNameInput: '',
      teamTwoScore: 0
    }
  },
  methods: {
    updateTeamOneName:function () {
      this.teamOneName = this.teamOneNameInput
      this.teamOneNameInput = ''
    },
    updateTeamTwoName:function () {
      this.teamTwoName = this.teamTwoNameInput
      this.teamTwoNameInput = ''
    },
    addOneToTeamOneScore:function () {
      this.teamOneScore++
    },
    addOneToTeamTwoScore:function () {
      this.teamTwoScore++
    },
    subOneFromTeamOneScore:function () {
      if (this.teamOneScore > 0) {
        this.teamOneScore--
      }
    },
    subOneFromTeamTwoScore:function () {
      if (this.teamTwoScore > 0) {
        this.teamTwoScore--
      }
    },
  }
}
</script>

<style scoped>
.teams {
  display: flex;
  justify-content: space-evenly;
}

.team-score {
  font-size: 48px;
}

.team-update-score-buttons {
  display: flex;
  justify-content: space-evenly;
}
</style>
