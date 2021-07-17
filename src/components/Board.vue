<template>
  <div>
    <status :winner="winner.player" :player="player" :isDrawGame="DrawGame"/>
    <div class="container">
      <field v-for="(field, index) in fields" :key="index" :value="field" v-on:click="change(index)"/>
  </div>
  <button @click="restart">Restart</button>
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
          key: 0,
      }
    },
    methods: {
    change(index) {
      if (this.fields[index]){
        return
      }
      this.$set(this.fields, index, this.player);
        this.player = this.player === "X" ? "O": "X";
        },
    restart(){
      this.player = "X";
      this.fields = Array(9).fill(null);
      }
    },
    computed: {
      winner(){
        return getWinner(this.fields);
      },
      DrawGame(){
        return this.fields.filter(field => !field).length === 0;
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