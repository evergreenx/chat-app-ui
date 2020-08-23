<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
  
      </v-col>

      <v-col>
        <form v-on:submit="getq">
          <input type="text" placeholder="Enter query" v-model="search" />
        </form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data() {
    return {
      search: ""
    };
  },
  mounted() {
    alert(this.search);
  },

  methods: {
    getq(e) {

      e.preventDefault()
      console.log(this.search);
    }
  }
};
</script>
