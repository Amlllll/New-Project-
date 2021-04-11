<template>
    <div class="film-card my-3">
        <div class="card" >
  <img :src="movie.image" class="card-img-top" >
  <div class="card-body">
    <h5 class="card-title">{{movie.title}}</h5>
    <p class="card-text">{{movie.preview}}</p>
   <router-link class="btn btn-primary" tag="button" :to="`/movies/${movie.id}`">Go</router-link>
  </div>
</div>
        
    </div>
</template>
<script>

export default{
    props:['movie'],
   name : "Card",
   
}
</script>
