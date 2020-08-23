<template>
  <div class="home">
    <v-app>
      <SearchCmp msg="Welcome to Your Vue.js App" />

      <v-container class="container-fluid">
        <div class="row">
          <div class="col-lg-4 mt-5" v-for="card in cards" :key="card.title">
            <v-card  @click="overlay = !overlay">
              <v-img
                :src="card.src"
                class="white--text align-end img-fluid"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="400px"
              >
                <v-card-title v-text="card.title"></v-card-title>
              </v-img>
            </v-card>
          </div>
        </div>

        <div class="text-center">
          <v-btn color="error" @click="overlay = !overlay">Show Overlay</v-btn>

          <v-overlay :value="overlay">
            <v-btn icon @click="overlay = false">
              x

              <!-- <img :src="card.src" > -->
            
            </v-btn>
          </v-overlay>
        </div>
      </v-container>
    </v-app>
  </div>
</template>

<script>
// @ is an alias to /src
import SearchCmp from "@/components/Search.vue";
import axios from "axios";

export default {
  name: "Home",

  data() {
    return {
      overlay:false,
      cards: [
        {
          title: "Pre-fab homes",
          src: "https://cdn.vuetifyjs.com/images/cards/house.jpg",
          flex: 6
        },
        {
          title: "Favorite road trips",
          src: "https://cdn.vuetifyjs.com/images/cards/road.jpg",
          flex: 4
        },
        {
          title: "Best airlines",
          src: "https://cdn.vuetifyjs.com/images/cards/plane.jpg",
          flex: 4
        }
      ]
    };
  },
  components: {
    SearchCmp
  },

  created() {
    axios.get();
  }
};
</script>


<style scoped>
.col-x .v-card {
  height: 200px;
}
</style>