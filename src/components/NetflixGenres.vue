<template>
  <div class="hello">
    <h1 style="color: #e50914">HELLO NETFLIX USER</h1>
    <div class="base-classify">
      <div class="new-tryout" v-for="(genre, idx) in netflix" :key=idx>
            <a class="genres" :href=genre.url target="_blank">
              <span class="centerize">{{genre.name}} </span></a>
      </div>
      <button class="more" @click="addingData()">
        daha fazla göster
      </button>
    </div>
  </div>
</template>

<script>
import json from '../../static/netflix.json'
export default {
  name: 'NetflixGenres',
  props: {
    msg: String
  },
  data() {
    return {
      netflix: json.slice(0 , 20),
      firstSlice: 20
    }
  },
  methods:{
    addingData(){
      this.firstSlice += 20
      this.netflix = json.slice(0 , this.firstSlice)
    },
  }

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
.base-classify{
  display: flex;
  flex-wrap: wrap;
  align-content: center;
  justify-content: center;
  padding-bottom: 300px;
}
.new-tryout{
  display: flex;
  align-content: center;
  justify-content: center;
  padding: 10px;

}
.centerize{
  position: relative;
  top: 15px;
}
.genres {
  width: 400px !important;
  height: 50px;
  color: black;
  text-align: center;
  border: 1px solid black;
  border-radius: 12px;
  background: white;
  text-decoration: none;
  padding: 20px;
}
.more{
  padding: 20px;
  text-transform: uppercase;
  border: none;
  border-radius: 12px;
  font-size: 30px;
}
.more:hover , a:hover{
  transition: 0.25s;
  cursor: pointer;
  background-color: #1DA1F2;
  color: white;
  border:none
}
@media (max-width:460px) {
  .genres{
    width:250px !important
  }
}
</style>
