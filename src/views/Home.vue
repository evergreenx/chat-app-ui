<template>
  <v-app class="container">
    <div class="row">
      <div class="col-lg-1">
        <Sidenav></Sidenav>
      </div>
      <div class="col-lg-3">
        <Chats></Chats>
      </div>
      <div class="col-lg-5">
        <ChatArea></ChatArea>
      </div>

      <div class="col-lg-3">
        <Userinfo></Userinfo>
      </div>
    </div>
  </v-app>
</template>

<style>
</style>

<script>
import Chats from "../components/Chats";
import Sidenav from "../components/Sidenav";
import Userinfo from "../components/Userinfo";
import ChatArea from "../components/ChatArea";

export default {
  components: {
    Chats,
    Sidenav,
    Userinfo,
    ChatArea
  }
};
</script>

<style>


</style>