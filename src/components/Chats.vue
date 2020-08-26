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

     <div class="buttonInside">
    <input placeholder="Type something" type="search" class="inputx">
    <button id="showPassword"><i class="fa fa-search buttonx" aria-hidden="true"></i></button>
  </div>
    


    <div class="user" v-for="(currentchat , index) in currentchats" :key="index">
        <v-avatar size="31px">    <img src="../assets/user.jpg"  /></v-avatar>

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
  background-color: #fff;
  display: flex;
  width: 100%;
  color: black;
  justify-content: space-around;
  padding: 10px;
  border-radius: 10px;
  margin: 2px 0px 20px 0px;
  outline: none;
}
.fa-plus{
  color:blue;
}

.buttonx{
  position:absolute;
  right: 12px;
  top: 14px;
  border:none;
  height:20px;
  width:20px;
  border-radius:100%;
  outline:none;
  text-align:center;
  font-weight:bold;
  padding:2px;
}
.buttonInside{
  position:relative;
  margin-bottom:10px;
}
.inputx{
  height:25px;
  width:100%;
  padding:23px;
  border-radius: 4px;
  border:none;outline:none;
  background-color: rgb(180, 169, 169);
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