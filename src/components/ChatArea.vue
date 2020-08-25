<template>
  <div>
    <section class="header">
      <div class="leftx">
        <v-badge bordered color="green  accent-4" dot bottom offset-x="10" offset-y="10">
          <v-avatar size="31px">
            <img src="../assets/user.jpg" alt="user" />
          </v-avatar>
        </v-badge>

        <span class="mx-2">Fernado Gaudo</span>
      </div>

      <div class="rightx">
        <span>Members :</span>
        <i class="fa fa-plus"></i>

        <v-avatar size="31px">
          <img src="../assets/user.jpg" alt="user" />
        </v-avatar>
        <i class="fas fa-cog"></i>
      </div>
    </section>

    <div class="chatarea" v-for="chat in userreplys " :key="chat.id">
      <div class="chat">
        {{chat.message}}
        <br />

        <span class="chat-time">16 mins ago</span>
        <span class="chat-timex">Seen 1:03pm</span>
      </div>

      <v-badge bordered color="green accent-4" dot bottom offset-x="10" offset-y="10">
        <v-avatar size="31px" class="chat-img mx-2">
          <img src="../assets/user.jpg" alt="user" />
        </v-avatar>
      </v-badge>
    </div>


<div>
      <v-badge bordered color="green accent-4" dot bottom offset-x="10" offset-y="10">

    <v-avatar size="31px" class="chat-img mx-2">
        <img src="../assets/user.jpg" alt="user" />
    </v-avatar>

      </v-badge>

</div>
    <div class="d-flex justify-space-around" v-for="chatx in replys " :key="chatx.id">
      <span class="chat-x">{{chatx.message}}

      <img :src="chatx.img" alt="image" class="img-res">
      </span>

      <i class="fas fa-ellipsis-h icon"></i>
    </div>
  </div>
</template>


<script>
import userreply from "../../src/ChatDb/userreply.json";
import reply from "../../src/ChatDb/reply.json";

export default {
  data() {
    return {
      userreplys: userreply,
      replys: reply
    };
  }
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
}

.header span {
  font-size: 13px;
}

.v-avatar {
  width: 20%;
}
.right-border {
  border-right: 3px solid;
  /* margin-left:200px */
}

.chat {
  border-radius: 21px 21px 0px 14px;
  -moz-border-radius: 21px 21px 0px 14px;
  -webkit-border-radius: 21px 21px 0px 14px;
  border: 0px solid #000000;
  background-color: blue;
  padding: 20px;
  width: 60%;
  color: #fff;
  margin-top: 30px;
}

.chat-x {
  border-radius: 21px 21px 14px 0px;
  -moz-border-radius: 21px 21px 14px 0px;
  -webkit-border-radius: 21px 21px 14px 0px;
  border: 0px solid #000000;
  background-color: grey;
  padding: 20px;
  width: 60%;
  color: #fff;
  margin-top: 30px;
}

.icon {
  margin-top: 50px;
}
.chat-img {
  top: 85px;
}

.chatarea {
  display: flex;
  justify-content: flex-end;
}

.chat-time {
  font-size: 12px;
  color: rgba(255, 255, 255, 0.435);
}

.chat-timex {
  margin-left: 80px;
  font-size: 12px;
  color: rgba(255, 255, 255, 0.435);
}

.img-res{
  width:80%;
  /* height:40%; */
}
</style>