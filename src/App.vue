<template>
  <div id="app">
    Powered by
    <img alt="Vue logo" src="./assets/logo.png" class="logo"/>
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: "App",
  components: {
  },
  data() {
    return {
    }
  },
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
</style>