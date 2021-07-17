<template>
  <div class="statusBar">
    <span v-if="winner">{{winner}} won!</span>
    <span v-else-if="isDrawGame">It's a draw.</span>
    <span v-else>Next player is {{player}}</span>
  </div>
</template>

<script>
export default {
  props: {
      winner: String,
      player: String,
      isDrawGame: Boolean
  }
}
</script>

<style lang="scss">
  .statusBar{
      margin-top: 30px;
  }
</style>