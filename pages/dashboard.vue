<template>
  <v-app>
    <v-navigation-drawer app clipped>
      <v-list>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list>
        <v-list-item v-for="item in itemsTemplate" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list>
        <v-list-item v-for="item in itemsHelp" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar class="app-bar" app clipped-left color="#6c3dff">
      <v-toolbar-title>
        <v-icon color="#fff">mdi-arrow-left</v-icon>
        Vue Material Admin
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn icon color="#fff">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon color="#fff">
        <v-icon>mdi-bell-outline</v-icon>
      </v-btn>
      <v-btn icon color="#fff">
        <v-icon>mdi-email-outline</v-icon>
      </v-btn>
      <div class="user-welcome-message">
        <span>Hi, <strong>John Smith</strong></span>
      </div>

      <v-avatar color="primary" size="45">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
    </v-app-bar>

    <v-main>
      <v-container fluid>
        <NavigationVcard />

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
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import NavigationVcard from "../components/navigation-vcard.vue";
import PerfilVcard from "../components/perfil-vcard.vue";
import FilesVcard from "../components/files-vcard.vue";
import MediaProjectsVcard from "../components/media-projects-vcard.vue";
import InformativeVcard from "../components/informative-vcard.vue";
import TasksVcard from "../components/tasks-vcard.vue";

export default Vue.extend({
  data() {
    return {
      items: [
        { title: "Profile", icon: "mdi-view-dashboard" },
        { title: "Dashboard", icon: "mdi-home" },
        { title: "E-Commerce", icon: "mdi-cart" },
        { title: "User", icon: "mdi-account" },
        { title: "Documentation", icon: "mdi-file-document" },
      ],
      itemsTemplate: [
        { title: "Core", icon: "mdi-apps" },
        { title: "Tables", icon: "mdi-grid-large" },
        { title: "UI Elements", icon: "mdi-image-filter-none" },
        { title: "Forms", icon: "mdi-file-document" },
        { title: "Charts", icon: "mdi-chart-bar" },
        { title: "Maps", icon: "mdi-map" },
        { title: "Extra", icon: "mdi-star" },
        { title: "Menu Levels", icon: "mdi-folder" },
      ],
      itemsHelp: [
        { title: "Library", icon: "mdi-book-variant-multiple" },
        { title: "Support", icon: "mdi-forum" },
        { title: "FAQ", icon: "mdi-help-circle-outline" },
      ],
      right: null,
    };
  },
  components: {
    NavigationVcard,
    PerfilVcard,
    FilesVcard,
    MediaProjectsVcard,
    InformativeVcard,
    TasksVcard,
  },
});
</script>

<style scoped>
.user-welcome-message {
  margin-right: 5px;
}

.app-bar {
  color: #fff;
}
</style>