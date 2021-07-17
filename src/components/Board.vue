<template>
  <div>
    <status :winner="winner.player" :player="player"/>
    <div class="container">
      <field v-for="(field, index) in fields" :key="index" :value="field" v-on:click="change(index)"/>
  </div>
  </div>
</template>

<script>
    import field from './Field.vue';
    import status from './Status.vue';
    import getWinner from '../winner'

export default {
    name: "board",
    components: { 
        field,
        status
    },
  data(){
      return{
          player:"X",
          fields: Array(9).fill(null),
          isDrawGame: false,
      }
    },
    methods: {
    change(index) {
      if (this.fields[index]){
        return
      }
      this.$set(this.fields, index, this.player);
        this.player = this.player === "X" ? "O": "X";
        }
    },
    computed: {
      winner(){
        return getWinner(this.fields)
      }
    }
};
</script>

<style lang="scss">
.container{
  width: 350px;
  height: 350px;
  margin: 0 auto;
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
}
</style>