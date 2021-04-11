<template>
    <div class="container" v-if="movie">
        <div class="my-3 mx-auto">
            <img :src="movie.image" class="img-fluid" />
            <h3 class="py-2">{{movie.title}}</h3>
            <h6 class="text-muted">{{movie.date}}</h6>
            <p class="py-1">{{movie.content}}</p>
        </div>
    </div>
</template>
<script>
import axios from 'axios'
export default ({
    data(){
        return{
            movie: null
        }

    },
  computed:{
      movieId(){
          return this.$route.params.id;
      }
  },
  mounted(){
      console.log(this.$route)
      axios.get(`https://movie-library-7e5ec.firebaseio.com/posts/${this.movieId}.json`)
        .then(res => {
           this.movie = {...res.data};
        }).catch(err => {
            console.log(err)
        })
  }
})
</script>

<style scoped>

</style>