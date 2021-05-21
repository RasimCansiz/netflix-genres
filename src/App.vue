<template>
  <div id="app">
    <netflix-genres :msg=msg></netflix-genres>
  </div>
</template>

<script>
import NetflixGenres from './components/NetflixGenres.vue'

export default {
  name: 'App',
  components: {
    NetflixGenres
  },
  data() {
    return {
      msg : 'selam'
    }
  },
}
</script>
<style lang="scss">
 @import "./assets/sass/general.scss";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
