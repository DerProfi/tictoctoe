<template>
  <div>
    <div class="container">
      <field v-for="(field, index) in fields" :key="index" v-on:click="change"/>
    </div>
  </div>
</template>

<script>
    import field from './Field.vue';

export default {
    name: "board",
    components: {
        field
    },
  data(){
      return{
          fields: Array(9).fill(null)
      }
    },
    methods: {
    change() {
      alert('test')
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