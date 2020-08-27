<template>
  <nav>
    <!-- <img src="../assets/logox.svg"> -->
    <div class="sidenav">

      <div class="icon-pack">
      <a href="#">
        <i class="far fa-file-alt"></i>
      </a>
      <a href="#">
        <i class="far fa-calendar-alt"></i>
      </a>
      <a href="#">
        <i class="far fa-comment-alt text-primary"></i>
      </a>
      <a href="#">
        <v-badge bordered top color="green accent-4" dot offset-x="10" offset-y="10">
          <i class="far fa-bell"></i>
        </v-badge>
      </a>
      </div>

      <div class="icon-pack">
      <a href="#">
        <i class="fa fa-users"></i>
      </a>
      <a href="#">
        <i class="fas fa-cog"></i>
      </a>

      <a href="#">
        <v-badge bordered bottom color="green accent-4" dot offset-x="10" offset-y="10">
          <v-avatar size="34">
            <img src="../assets/user.jpg" alt="user-avatar" />
          </v-avatar>
        </v-badge>
      </a>

      </div>
    </div>
  </nav>
</template>


<script>
export default {};
</script>

<style scoped>
nav {
  height: 100%;
  width: 60px;
  position: relative;
  z-index: 1;
  top: 0;
  left: 0;
  /* background-color:#fff; */
  overflow-x: hidden;
  /* padding-top: 20px; */
  
}

.sidenav a {
  padding: 6px 6px 6px 6px;
  text-decoration: none;
  font-size: 25px;
  color: #818181;
  display: block;
}



.icon-pack{
  margin-top: 150px;
} .nav{
  background-color: khaki;
}

@media screen and (max-width: 700px) {
  nav {
    width: 100%;
    height: auto;
    position: relative;
  }
  nav a {float: left; margin-top:0;}
  div.content {margin-left: 0;}
}

@media screen and (max-width: 400px) {
  .nav a {
    text-align: center;
    float: none;
    margin-left: 0;
  }
}
</style>