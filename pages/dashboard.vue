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