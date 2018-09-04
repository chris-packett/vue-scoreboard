<template>
  <div class="team-update-container">
    <div class="team-update-name">
      <h4>Update Team Name:</h4>
      <div class="team-update-name-input-and-button">
        <input type="text" placeholder="Update team name..." value="">
        <button>Update</button>
      </div>
    </div>
    <div class="team-update-score">
      <h4>Update Team Score:</h4>
      <div class="team-update-score-buttons">
        <button>Add 1</button>
        <button>Subtract 1</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Update"
}
</script>

<style scoped>
.team-update-score-buttons {
  display: flex;
  justify-content: space-evenly;
}
</style>
