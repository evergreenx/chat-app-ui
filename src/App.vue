<template>
  <v-app>
 
<Home/>



  </v-app>
</template>

<script> 
import Home from "./views/Home";

export default {
  name: "App",

  data(){
    return{
      name:'john'

    }
  },
  components: {
    Home
  }

,
  
};
</script>


<style>

@import './assets/b4/bootstrap.min.css';

body{
  background-color:grey;
}


</style>