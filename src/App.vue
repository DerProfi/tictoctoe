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
