<template>
  <div id="app">
    Powered by
    <img alt="Vue logo" src="./assets/logo.png" class="logo"/>
    <div class="container">
      <field v-for="field in fields" :key="field.id" @click="change"/>
    </div>
    <button>Restart</button>
   
  </div>
</template>

<script>
import field from './components/Field.vue';

export default {
  name: "App",
  components: {
    field
  },
  data() {
    return {
      fields: [
        {
          id: 1,
          cross: false,
          circle: false
        },
        {id: 2,
          cross: false,
          circle: false},
        {id: 3,
          cross: false,
          circle: false},
        {id: 4,
          cross: false,
          circle: false},
        {id: 5,
          cross: false,
          circle: false},
        {id: 6,
          cross: false,
          circle: false},
        {id: 7,
          cross: false,
          circle: false},
        {id: 8,
          cross: false,
          circle: false},
        {id: 9,
          cross: false,
          circle: false}
      ]
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
* {
  margin: 0;
  padding: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.logo{
  width: 50px;
}

.container{
  width: 350px;
  height: 350px;
  margin: 0 auto;
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
}
</style>
