<template>
  <v-main class="box-content">
    <v-card class="login">
      <v-bottom-navigation
        class="navigation-buttons"
        color="#6c3dff"
        horizontal
        grow
      >
        <v-btn class="button-menu-login">
          <span>LOGIN</span>

          <v-icon>mdi-account-arrow-right</v-icon>
        </v-btn>

        <v-btn class="button-menu-login">
          <span>NEW USER</span>

          <v-icon>mdi-account-multiple-plus</v-icon>
        </v-btn>

         <v-btn class="button-menu-login" :to="'/dashboard'">
          <span>DASHBOARD</span>

          <v-icon>mdi-view-dashboard</v-icon>
        </v-btn>
      </v-bottom-navigation>

      <v-card-title class="welcome-user">
        <h1>Good Morning, User</h1>
        <v-btn color="#ffffff" class="sign-in" block elevation="2">
          <v-icon dark left>mdi-google</v-icon> Sign in With Google</v-btn
        >
      </v-card-title>
      <v-card-text>
        <v-row>
          <v-col>
            <v-divider
              role="separator"
              aria-orientation="horizontal"
            ></v-divider>
          </v-col>

          <span>Or</span>

          <v-col>
            <v-divider
              role="separator"
              aria-orientation="horizontal"
            ></v-divider>
          </v-col>
        </v-row>

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
        <v-btn class="botton-login" color="#6c3dff">Login</v-btn>
        <v-btn class="botton-password" outlined color="#6c3dff">
          Forget Password
        </v-btn>
      </v-card-actions>
    </v-card>
    <v-footer absolute color="#fff">
      <v-col class="footer-page">
        &copy; 2014-2020 Flatlogic, LLC. All rights reserved
      </v-col>
    </v-footer>
  </v-main>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
.navigation-buttons {
  box-shadow: none;
}
.box-content {
  height: 800px;
  margin-top: 50px;
  font-family: Roboto, sans-serif;
}
.login {
  margin-top: 150px;
  margin-left: 100px;
  margin-right: 100px;
}
span {
  font-size: 15px;
}
.botton-login {
  color: #fff;
}
.botton-password {
  position: absolute;
  right: 10px;
}
.welcome-user {
  justify-content: center;
  height: 250px;
}
.footer-page {
  text-align: center;
  color: #6c3dff;
}
</style>