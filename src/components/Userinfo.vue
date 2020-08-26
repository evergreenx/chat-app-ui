<template>
  <section>
    <div class="card">
      <div class="card-body text-center">
        <div class="user-img">
           <v-avatar>
      <img
        src="../assets/user.jpg"
        alt="John"
      >
    </v-avatar>
        </div>
        <h5 class="card-title">Fernado Gaudo</h5>
        <p class="card-text text-muted">CEO & Founder at Highly inc</p>
      </div>
    </div>

    <div>
      <v-expansion-panels>
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h5>Information</h5>
          </v-expansion-panel-header>
          <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </div>

    <div>
      <v-expansion-panels>
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h5>Images(5)</h5>
          </v-expansion-panel-header>
          <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </div>

    <div>
      <v-expansion-panels v-model="panel" :disabled="disabled" multiple>
        <v-expansion-panel>
          <v-expansion-panel-header>
            <h5>Files(3)</h5>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
         
         <i class="fa fa-download"></i>
            <p>Landing_Page.pdf</p>
            <br />

<i class="fa fa-download"></i>
            <p>Requirement.zip</p>
            <br />

            <i class="fa fa-download"></i>
            <p>Uwagi.docx</p>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </div>

    <v-expansion-panels>
      <v-expansion-panel>
        <v-expansion-panel-header>
          <h5>Pinned Item</h5>
        </v-expansion-panel-header>
        <v-expansion-panel-content>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </section>
</template>


<script>
export default {
  data() {
    return {
      panel: [0, 1],
      disabled: false,
      readonly: false
    };
  }
};
</script>

<style scoped>
.img-circle {
  width: 70px;
  border-radius: 200px;
  margin: auto;
}

.card {
  /* background-color: grey; */
  border: none;
  margin-top: 20px;

   box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  text-align: center;
}
.v-expansion-panel {
  background-color: red;
  margin-top: 20px;
}

p {
  font-weight: 400;
}
h5{
  font-size: 14px;
}

</style>

