<template>
  <div id="app">
    <div id="nav">
      <h1>{{ getIsMobile ? 'Mobile' : 'Desktop' }}</h1>
    </div>
    <router-view/>
  </div>
</template>

<script>
import isMobile from '@/utils/isMobile'

export default {
  name: 'App',

  computed: {
    getIsMobile() {
      return isMobile()
    }
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  h1 {
    font-size: 3em;
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
