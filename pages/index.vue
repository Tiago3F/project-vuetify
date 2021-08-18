<template>
  <div>
    <v-container>
      <v-row>
        <v-col md="7"> <LogoText /> </v-col>
        <v-col  md="5"> <Login /> </v-col>
      </v-row>
    </v-container>
  </div>
</template>




<script lang="ts">
import Vue from "vue";
import Login from "./login.vue";
import LogoText from "./logotext.vue";

export default Vue.extend({
  components: {
    Login,
    LogoText,
  },
});
</script>

<style scoped>
</style>
