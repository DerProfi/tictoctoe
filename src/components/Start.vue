<template>
  <div class="welcomeScreen">
      <hr>
      <span>Welcome to the game!</span>
      <br>
      <span>How would you like to play?</span>
      <br>
      <button>PvE</button>
      <label for="singlePlayer"></label>
      <router-link to="/board" tag="button">PvP</router-link>
      
  </div>
</template>

<script>
export default {
    name: "start"
}
</script>

<style>
hr{
    margin-top: 20px;
    margin-bottom: 10px;
}
.welcomeScreen{
    width: 50%;
    margin: 0 auto;
}

button{
    margin: 10px;
    padding: 5px;
    border: none;
    color: white;
    background-color: grey;
}
</style>