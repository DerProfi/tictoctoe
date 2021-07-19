<template>
  <div class="statusBar">
    <span v-if="winner">{{ winner }} won!</span>
    <span v-else-if="isDrawGame">It's a draw.</span>
    <span v-else-if="playerOne">Next player is {{ playerOne }}</span>
    <span v-else>Please enter your names.</span>
  </div>
</template>

<script>
export default {
  data(){
    return {
    currentPlayer: "",  
    playerOne: "",
    playerTwo: "",
    };
  },
  props: {
    winner: String,
    player: String,
    isDrawGame: Boolean,
  },
  mounted(){
    if (localStorage.playerOne) {
      this.playerOne = localStorage.playerOne;
    }
    if (localStorage.playerTwo) {
      this.playerTwo = localStorage.playerTwo;
    }
  },
  methods: {
    //Currently not working
    //   currentlyPlaying(){
    //   this.currentPlayer = this.currentPlayer === this.playerOne ? this.playerTwo : this.playerOne;
    // }
  }
};
</script>

<style lang="scss">
.statusBar {
  margin-top: 30px;
}
</style>
