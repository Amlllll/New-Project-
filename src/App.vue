<template>
  <div id="app">
    <div id="nav">
      <NavbarProject></NavbarProject>
    </div>

    <router-view />
 
  </div>
</template>
<script>

import NavbarProject from '@/components/NavbarProject'

export default ({
  data: function(){
    return{

    }

  },
  components:{
      NavbarProject
    }
  
})
</script>


<style >

</style>
