<template>
    <div>
        <v-row no-gutters>
          <v-col md="5">
            <PerfilVcard />
            <MediaProjectsVcard />
            <InformativeVcard />
          </v-col>
          <v-col md="7">
            <FilesVcard />
            <TasksVcard />
          </v-col>
        </v-row>
      <v-footer height="80px" color="#fff">
        <v-row>
          <v-btn text color="#6c3dff" small>Flatlogic</v-btn>
          <v-btn text color="#6c3dff" small>About Us</v-btn>
          <v-btn text color="#6c3dff" small>Blog</v-btn>

          <v-spacer></v-spacer>

          <v-btn elevation="0" fab small>
            <v-icon>mdi-facebook</v-icon>
          </v-btn>

          <v-btn elevation="0" fab small>
            <v-icon>mdi-twitter</v-icon>
          </v-btn>

          <v-btn elevation="0" fab small>
            <v-icon>mdi-github</v-icon>
          </v-btn>
        </v-row>
      </v-footer>
    </div>
</template>

<script lang="ts">
import PerfilVcard from "../components/perfil-vcard.vue";
import FilesVcard from "../components/files-vcard.vue";
import MediaProjectsVcard from "../components/media-projects-vcard.vue";
import InformativeVcard from "../components/informative-vcard.vue";
import TasksVcard from "../components/tasks-calendar-vcard.vue";


export default {
  data() {
    return {
     
    };

  },
  components: {

    PerfilVcard,
    FilesVcard,
    MediaProjectsVcard,
    InformativeVcard,
    TasksVcard,

  },
};
</script>

<style scoped>

</style>