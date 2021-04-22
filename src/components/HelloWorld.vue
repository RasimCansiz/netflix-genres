<template>
  <div class="hello">
    <h1>HELLO NETFLIX USER</h1>
    <div v-for="(genre, idx) in netflix" :key=idx><a :href=genre.url target="_blank">{{genre.name}} </a></div>
  </div>
</template>

<script>
import json from '../../static/netflix.json'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      netflix: json
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
