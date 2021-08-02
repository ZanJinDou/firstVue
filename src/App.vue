<template>
  <div id="app">
    <img v-show="show" src="@/assets/logo.png" alt="">
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
<script>
export default {
  name: 'App',
  data () {
    return {
      show: true
    }

  },
  watch: {
    $route (to, from) {
      if (to.path == "/") {
        this.show = true;
      } else {
        this.show = false;
      }
    }
  }
}
</script>
