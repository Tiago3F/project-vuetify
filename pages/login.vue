<template>
  <v-content class="box-content">
    <v-card class="login">
      <v-card-title class="welcome-user">
        <h1>Good Morning User</h1>
      </v-card-title>
      <v-card-text>
        <v-btn block elevation="2"> Sign in With Google</v-btn>
        <v-form>
          <v-text-field label="Username" prepend-icon="mdi-account-circle" />
          <v-text-field
            label="Password"
            prepend-icon="mdi-lock"
            append-icon="mdi-eye-off"
          />
        </v-form>
      </v-card-text>
      <v-card-actions>
        <v-btn class="botton-login">Login</v-btn>
      </v-card-actions>
    </v-card>
    <v-footer absolute>
      <v-col class="footer-page"> &copy; 2014-2020 Flatlogic, LLC. All rights reserved </v-col>
    </v-footer>
  </v-content>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
.box-content {
  height: 800px;
  margin-top: 50px;
  background-color: #6c3dff;
}
.login {
  margin-top: 300px;
  margin-left: 100px;
  margin-right: 100px;
}
.botton-login {
  background-color: black;
}
.welcome-user {
  justify-content: center;
}
.footer-page {
  text-align: center;
  
}
</style>