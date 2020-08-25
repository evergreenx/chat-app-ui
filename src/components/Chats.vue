<template>
  <section>
    <button class="conversion">
      <span class="fa fa-plus mt-1"></span>

      <span>New conversion</span>
    </button>

    <div class="chat">
      <h2>Chats</h2>

      <i class="fas fa-ellipsis-h"></i>
    </div>

    <div class="input">
      <input type="search" class="form-control" placeholder="search here" />

      <div class="form-group has-search">
    <span class="fa fa-search form-control-feedback"></span>
    <input type="text" class="form-control" placeholder="Search">
  </div>
  
    </div>


    <div class="user" v-for="(currentchat , index) in currentchats" :key="index">
        <v-avatar size="31px">    <img src="../assets/user.jpg" alt="user" /></v-avatar>

<div class="userdata">
        <h5> 
{{currentchat.name}}


          <p class="text-mute"> 
{{currentchat.lastactive}}

          </p>
        </h5>
      
</div>

    </div>
      <hr/>

  </section>
</template>


<script>
export default {



  data(){
    return{

    currentchats:[
{

 name:'Tim hover' , 
 lastactive: '32 mins Ago'
} , 
{

 name:'Malian Zuch' , 
 lastactive: '4 Hour Ago'
}

,
{

 name:'Maria Valbuena' , 
 lastactive: '4 Hour Ago'
}
     ,
     {

 name:'Farnando' , 
 lastactive: '7 Hour Ago'
},

{

 name:'Lusi Monroe' , 
 lastactive: '10 Hour Ago'
} , 

{

 name:'Kate Lingard' , 
 lastactive: '13 Hour Ago'
} , 

{

 name:'Mario Benucci' , 
 lastactive: '4 Hour Ago'
} , 
{

 name:'Josh Trevor' , 
 lastactive: '23 Hour Ago'
}
    ]
      
    }
  }
};
</script>

<style scoped>

body{
  background-color:red;
}
.conversion {
  background-color: #000;
  display: flex;
  width: 100%;
  color: red;
  justify-content: space-around;
  padding: 10px;
  border-radius: 10px;
  margin: 2px 0px 20px 0px;
  outline: none;
}

.has-search .form-control-feedback {
    position: absolute;
    z-index: 2;
    display: block;
    width: 1.375rem;
    height: 2.375rem;
    line-height: 2.375rem;
    text-align: center;
    pointer-events: none;
    color: #aaa;
    /* float:left; */
}

.has-search .form-control {
    padding-left: 2.375rem;
}

.user{
  display: flex;
  box-sizing: content-box;
  border-bottom: 1px solid rgba(97, 96, 96, 0.346);
  width:80%;
  /* margin-top:20px; */
  padding:5px;
  
}



.user p{
  font-size:12;
}

.userdata{
  margin-left: 30px;
}

.text-mute{
  color:rgba(143, 143, 126, 0.496)
}

h5{
  font-size:14px
}

.chat{
  display:flex;
  justify-content: space-between;
}

.fa-ellipsis-h{

color:grey;
cursor:grabbing

}
</style>