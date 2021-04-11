<template>
    <div>
           <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <div class="container">
   <router-link to="/" class="navbar-brand">Navbar</router-link> |
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
     <router-link to="/" active-class="active" tag="a">Home</router-link> |
      <router-link to="/about" tag="a">About</router-link>
       <router-link to="/blog" tag="a">Blog</router-link>
    
      </ul>
      
    </div>
  </div>
</nav>
    </div>
</template>
<script>


export default ({
   name: "NavbarProject"
})
</script>
<style >
nav {

    font-family: 'El Messiri', sans-serif;
}
nav ul a {
    color: #fff;
    text-decoration: none;
    margin: 0 10px;
}
nav ul a:hover{
    color: crimson;
}
</style>
