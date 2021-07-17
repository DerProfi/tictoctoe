<template>
    <div class="option">
        <form>
          <label for="player1">Player 1: </label>
          <input type="text" id="player1" placeholder="Player1" v-model="playerOne">
          <label for="player2">Player 2: </label>
          <input type="text" id="player2" placeholder="Optional" v-model="playerTwo">
          <button @click="save">Save</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            playerOne: "",
            playerTwo: "",
        }
    },
    mounted() {
        if (localStorage.playerOne) {
            this.playerOne = localStorage.playerOne;
        }
        if (localStorage.playerTwo) {
            this.playerTwo = localStorage.playerTwo;
        }
    },
    methods: {
        save() {
            localStorage.playerOne = this.playerOne;
            localStorage.playerTwo = this.playerTwo;
        }
    }
}
</script>

<style>
.option{
    margin-top: 20px;
}
</style>