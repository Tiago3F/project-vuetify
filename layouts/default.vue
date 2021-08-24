<template>
  <v-app>
    <v-app-bar
      v-if="$route.path != '/'"
      class="app-bar"
      app
      clipped-left
      color="#6c3dff"
    >
      <v-toolbar-title>
        <v-icon color="#fff">mdi-arrow-left</v-icon>
        Vue Material Admin
      </v-toolbar-title>
      <v-spacer></v-spacer>

      <v-btn icon color="#fff">
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon color="#fff">
        <v-icon> mdi-bell-outline</v-icon>
        <span class="notify-bell">4</span>
      </v-btn>
      <v-btn icon color="#fff">
        <v-icon>mdi-email-outline</v-icon>
        <span class="notify-message">3</span>
      </v-btn>
      <div class="user-welcome-message">
        <span>Hi, <strong>John Smith</strong></span>
      </div>

      <v-avatar color="primary" size="45">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
    </v-app-bar>

    <v-navigation-drawer v-if="$route.path != '/'" app clipped fixed>
      <v-list>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          route
          :to="item.route"
        >
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
        <v-list-item v-for="item in itemsTemplate" :key="item.title" router>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-group prepend-icon="mdi-file-document" value="true">
          <v-list-tile slot="activator">
            <v-list-tile-title>Forms</v-list-tile-title>
          </v-list-tile>
          <v-list-item v-for="form in forms" :key="form.title" :to="form.route">
            <v-icon>mdi-circle-small</v-icon> {{ form.title }}</v-list-item
          >
        </v-list-group>
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
    <v-main>
      <v-container fluid>
        <NavigationVcard v-if="$route.path != '/'" />
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>
<script>
import NavigationVcard from "../components/navigation-vcard.vue";

export default {
  layout: "default",
  data() {
    return {
      items: [
        { title: "Profile", icon: "mdi-view-dashboard" },
        { title: "Dashboard", icon: "mdi-home", route: "/dashboard" },
        { title: "E-Commerce", icon: "mdi-cart" },
        { title: "User", icon: "mdi-account" },
        { title: "Documentation", icon: "mdi-file-document" },
      ],
      itemsTemplate: [
        { title: "Core", icon: "mdi-apps" },
        { title: "Tables", icon: "mdi-grid-large" },
        { title: "UI Elements", icon: "mdi-image-filter-none" },
        // { title: "Forms", icon: "mdi-file-document", route: "/forms" },
        { title: "Charts", icon: "mdi-chart-bar" },
        { title: "Maps", icon: "mdi-map" },
        { title: "Extra", icon: "mdi-star" },
        { title: "Menu Levels", icon: "mdi-folder" },
      ],
      forms: [{ title: "Form Elements", route: "/forms" }, { title: "Form Validation" }],

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
  },
};
</script>
<style scoped>
.user-welcome-message {
  margin-right: 5px;
}

.app-bar {
  color: #fff;
}

.notify-bell {
  border-radius: 10px;
  font-size: 12px;
  height: 20px;
  letter-spacing: 0;
  min-width: 20px;
  padding: 4px 6px;
  pointer-events: auto;
  position: absolute;
  text-align: center;
  text-indent: 0;
  margin-left: 25px;
  margin-top: -25px;
  background-color: #ff4081;
}
.notify-message {
  border-radius: 10px;
  font-size: 12px;
  height: 20px;
  letter-spacing: 0;
  min-width: 20px;
  padding: 4px 6px;
  pointer-events: auto;
  position: absolute;
  text-align: center;
  text-indent: 0;
  margin-left: 25px;
  margin-top: -25px;
  background-color: #ffc260;
}
</style>