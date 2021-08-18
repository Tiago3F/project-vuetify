<template>
  <v-content class="logo-text">
    <v-img class="image"
      src='https://templates-flatlogic.herokuapp.com/vue-material/img/logo.3d432ca2.svg'
      max-height="300"
      max-width="150"
    ></v-img>
    <h1>Vue Material Admin</h1>
  </v-content>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
.logo-text {
  height: 800px;
  margin-top: 50px;
  background-color: #6c3dff;
  }

h1 {
  text-align: center;
  color: #fff;
  font-size: 50px;
}

.image {
   margin-left: 430px;
   margin-top: 250px;
}
</style>