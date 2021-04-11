<template>
  <div class="home py-5">
    <div class="container">
      <h2>Films</h2>
      <div class="row" v-if="movies.length > 0" >
        <div class="col-md-4" v-for="movie in movies" :key="movie.id">

          <Card :movie="movie"></Card>
        </div>
        </div>
        <div v-else>No Movies yet</div>

    </div>
    
   
  </div>
</template>

<script>
// @ is an alias to /src

import Card from '../components/Card.vue';
import axios from 'axios';

export default {
  name: "Home",
  data(){
    return{
     movies: []
    }
  },
  mounted(){
      axios.get(`https://movie-library-7e5ec.firebaseio.com/posts.json`)
        .then(res => {
           for (let key in res.data){
             this.movies.push({...res.data[key], id: key })
           }
        }).catch(err => {
            console.log(err)
        })
  },
  components: {
    Card
    
},
};
</script>
<style >
.home{
  font-family: 'El Messiri', sans-serif;
}

</style>
