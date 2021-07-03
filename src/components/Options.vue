<template>
    <div class="option">
        <label for="player1">Player 1: </label>
        <input type="text" id="player1" placeholder="Player1" v-model="playerOne">
        <label for="player2">Player 2: </label>
        <input type="text" id="player2" placeholder="Player2" v-model="playerTwo">
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
}
</script>

<style>
.option{
    margin-top: 20px;
}
</style>