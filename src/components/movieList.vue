<template>
  <ul id="example-1">
    <li v-for="item in movies">
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'movieList',
  data () {
    return {
      movies:[1,2,3],
      getMoviesUrl:"http://118.24.11.218:8080/api/movies"
    }
  },
  mounted() {
    //this.getMovies()
  },
  methods: {
    getMovies(){
      this.movies="[1,2,3]"
//      var that = this;
//      that.$http({           //调用接口
//        method:'GET',
//        url:this.getMoviesUrl  //this指data
//      }).then(function(response){  //接口返回数据
//        this.movies=response.data;
//      },function(error){
//      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
